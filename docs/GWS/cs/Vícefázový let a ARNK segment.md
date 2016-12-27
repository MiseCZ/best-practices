#Vícefázový let a ARNK segment

U vícefázového letu (klient si naplánuje svoji vlastní cestu s odlety z jiného místa, než kam přiletěl) je nutné vkládat tzv. ARNK segment, tj. neletový segment, který systému řekne, že je v pořádku, že lety na sebe nenavazují. Provede se to zařazením **<ARNKSellMods/>** mezi segmenty letu, kde se neletový segment nalézá.

Je nutné dát pozor na situaci, kdy je odlet pouze z jiného letiště v rámci stejného města. To není považováno jako přemístění na jiné místo a ARNK se tam nevkládá.

```
<AirSegSellMods>
  <AirSegSell>
    <Vnd>BA</Vnd>
    <FltNum>0855</FltNum>
    <OpSuf/>
    <Class>S</Class>
    <StartDt>20160706</StartDt>
    <StartAirp>PRG</StartAirp>
    <EndAirp>LHR</EndAirp>
    <StartTm>1115</StartTm>
    <EndTm>1230</EndTm>
    <Status>NN</Status>
    <DtChg>0</DtChg>
    <NumPsgrs>3</NumPsgrs>
    <AvailDispType>G</AvailDispType>
    <AvailJrnyNum>01</AvailJrnyNum>
  </AirSegSell>
  <AirSegSell>
    <Vnd>BA</Vnd>
    <FltNum>0279</FltNum>
    <OpSuf/>
    <Class>N</Class>
    <StartDt>20160706</StartDt>
    <StartAirp>LHR</StartAirp>
    <EndAirp>SJC</EndAirp>
    <StartTm>1525</StartTm>
    <EndTm>1815</EndTm>
    <Status>NN</Status>
    <DtChg>0</DtChg>
    <NumPsgrs>3</NumPsgrs>
    <AvailDispType>G</AvailDispType>
    <AvailJrnyNum>01</AvailJrnyNum>
  </AirSegSell>
  <!-- Zde je ARNK segment -->
  <ARNKSellMods/>
  <AirSegSell>
    <Vnd>BA</Vnd>
    <FltNum>0286</FltNum>
    <OpSuf/>
    <Class>N</Class>
    <StartDt>20160723</StartDt>
    <StartAirp>SFO</StartAirp>
    <EndAirp>LHR</EndAirp>
    <StartTm>1915</StartTm>
    <EndTm>1340</EndTm>
    <Status>NN</Status>
    <DtChg>1</DtChg>
    <NumPsgrs>3</NumPsgrs>
    <AvailDispType>G</AvailDispType>
    <AvailJrnyNum>02</AvailJrnyNum>
  </AirSegSell>
  <AirSegSell>
    <Vnd>BA</Vnd>
    <FltNum>0856</FltNum>
    <OpSuf/>
    <Class>S</Class>
    <StartDt>20160724</StartDt>
    <StartAirp>LHR</StartAirp>
    <EndAirp>PRG</EndAirp>
    <StartTm>1635</StartTm>
    <EndTm>1930</EndTm>
    <Status>NN</Status>
    <DtChg>0</DtChg>
    <NumPsgrs>3</NumPsgrs>
    <AvailDispType>G</AvailDispType>
    <AvailJrnyNum>02</AvailJrnyNum>
  </AirSegSell>
</AirSegSellMods>
```

