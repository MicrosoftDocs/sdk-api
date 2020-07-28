---
UID: NF:tuner.IScanningTunerEx.SetScanSignalTypeFilter
title: IScanningTunerEx::SetScanSignalTypeFilter (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["IScanningTunerEx interface [Microsoft TV Technologies]","SetScanSignalTypeFilter method","IScanningTunerEx.SetScanSignalTypeFilter","IScanningTunerEx::SetScanSignalTypeFilter","IScanningTunerExSetScanSignalTypeFilter","SetScanSignalTypeFilter","SetScanSignalTypeFilter method [Microsoft TV Technologies]","SetScanSignalTypeFilter method [Microsoft TV Technologies]","IScanningTunerEx interface","mstv.iscanningtunerex_setscansignaltypefilter","tuner/IScanningTunerEx::SetScanSignalTypeFilter"]
old-location: mstv\iscanningtunerex_setscansignaltypefilter.htm
tech.root: mstv
ms.assetid: 223a904a-1f15-4010-b25f-8551c1e9fc25
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],SetScanSignalTypeFilter method, IScanningTunerEx.SetScanSignalTypeFilter, IScanningTunerEx::SetScanSignalTypeFilter, IScanningTunerExSetScanSignalTypeFilter, SetScanSignalTypeFilter, SetScanSignalTypeFilter method [Microsoft TV Technologies], SetScanSignalTypeFilter method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_setscansignaltypefilter, tuner/IScanningTunerEx::SetScanSignalTypeFilter
f1_keywords:
- tuner/IScanningTunerEx.SetScanSignalTypeFilter
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tuner.h
api_name:
- IScanningTunerEx.SetScanSignalTypeFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScanningTunerEx::SetScanSignalTypeFilter


## -description



This topic applies to Windows Vista and later.
        



Not implemented in this release.
      

The <b>SetScanSignalTypeFilter</b> method specifies the type of signal to scan for. Applications can optionally call this method before calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>, to filter the signal types that the tuner will search for.


## -parameters




### -param ScanModulationTypes

Specifies the modulation types, as a bitwise OR of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/scanmodulationtypes">ScanModulationTypes</a> enumeration. If the value is 0xFFFFFFFF, the tuner does not filter out any specific modulation types.


### -param AnalogVideoStandard

Specifies the analog standards, as a bitwise OR of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration. If the value is 0xFFFFFFFF, the tuner does not filter out any specific analog video standards.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>
 

 

