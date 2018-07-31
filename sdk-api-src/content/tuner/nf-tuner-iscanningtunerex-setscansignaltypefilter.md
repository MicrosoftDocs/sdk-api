---
UID: NF:tuner.IScanningTunerEx.SetScanSignalTypeFilter
title: IScanningTunerEx::SetScanSignalTypeFilter
author: windows-sdk-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_setscansignaltypefilter.htm
old-project: mstv
ms.assetid: 223a904a-1f15-4010-b25f-8551c1e9fc25
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],SetScanSignalTypeFilter method, IScanningTunerEx.SetScanSignalTypeFilter, IScanningTunerEx::SetScanSignalTypeFilter, IScanningTunerExSetScanSignalTypeFilter, SetScanSignalTypeFilter, SetScanSignalTypeFilter method [Microsoft TV Technologies], SetScanSignalTypeFilter method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_setscansignaltypefilter, tuner/IScanningTunerEx::SetScanSignalTypeFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tuner.h
api_name:
 - IScanningTunerEx.SetScanSignalTypeFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx::SetScanSignalTypeFilter


## -description



This topic applies to Windows Vista and later.
        



Not implemented in this release.
      

The <b>SetScanSignalTypeFilter</b> method specifies the type of signal to scan for. Applications can optionally call this method before calling <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>, to filter the signal types that the tuner will search for.


## -parameters




### -param ScanModulationTypes

Specifies the modulation types, as a bitwise OR of flags from the <a href="https://msdn.microsoft.com/20101fa7-b943-4737-a6ec-a952bdf25196">ScanModulationTypes</a> enumeration. If the value is 0xFFFFFFFF, the tuner does not filter out any specific modulation types.


### -param AnalogVideoStandard

Specifies the analog standards, as a bitwise OR of flags from the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration. If the value is 0xFFFFFFFF, the tuner does not filter out any specific analog video standards.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

