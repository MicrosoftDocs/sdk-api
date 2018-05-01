---
UID: NF:tuner.IScanningTunerEx.GetTunerStatus
title: IScanningTunerEx::GetTunerStatus method
author: windows-driver-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_gettunerstatus.htm
old-project: mstv
ms.assetid: 9e91f5ca-5a2e-414e-bf4c-882ba6a08b98
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTunerStatus method [Microsoft TV Technologies], GetTunerStatus method [Microsoft TV Technologies], IScanningTunerEx interface, GetTunerStatus,IScanningTunerEx.GetTunerStatus, IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], GetTunerStatus method, IScanningTunerEx::GetTunerStatus, IScanningTunerExGetTunerStatus, mstv.iscanningtunerex_gettunerstatus, tuner/IScanningTunerEx::GetTunerStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tuner.h
api_name:
-	IScanningTunerEx.GetTunerStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx::GetTunerStatus method


## -description



This topic applies to Windows Vista and later.
        



The <b>GetTunerStatus</b> method returns the current status of the most recent call to <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>.


## -parameters




### -param SecondsLeft [out]

Receives the estimated number of seconds remaining for the scan to complete.


### -param CurrentLockType [out]

Receives a member of the <a href="https://msdn.microsoft.com/657dfd46-b01c-41aa-af0c-0d07235f15fc">TunerLockType</a> enumeration, indicating how well the tuner locked onto a signal.


### -param AutoDetect [out]

Receives a Boolean value. If the value is <b>TRUE</b>, the tuner is in auto-detect mode.


### -param CurrentFreq [out]

Receives the frequency that was most recently scanned.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



While the scan is in progress, the application can use this method to estimate the total time required for the scan to complete. When the tuner locks onto a frequency and sets the application's event handle, the application can use this method to find the locked frequency.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

