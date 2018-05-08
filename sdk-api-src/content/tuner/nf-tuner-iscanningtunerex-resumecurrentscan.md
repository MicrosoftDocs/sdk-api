---
UID: NF:tuner.IScanningTunerEx.ResumeCurrentScan
title: IScanningTunerEx::ResumeCurrentScan
author: windows-driver-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_resumecurrentscan.htm
old-project: mstv
ms.assetid: 9d855ae4-a49c-43d6-9ba0-9f6158f4034f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],ResumeCurrentScan method, IScanningTunerEx.ResumeCurrentScan, IScanningTunerEx::ResumeCurrentScan, IScanningTunerExResumeCurrentScan, ResumeCurrentScan, ResumeCurrentScan method [Microsoft TV Technologies], ResumeCurrentScan method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_resumecurrentscan, tuner/IScanningTunerEx::ResumeCurrentScan
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
-	IScanningTunerEx.ResumeCurrentScan
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx::ResumeCurrentScan


## -description



This topic applies to Windows Vista and later.
        



The <b>ResumeCurrentScan</b> method resumes scanning the range of frequencies specified in <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>.


## -parameters




### -param hEvent [in]

Handle to an event created by the application. When the tuner locks onto a signal, it signals this event.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
No scan has been started yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Invalid <i>hEvent</i> argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



When the application calls <b>PerformExhaustiveScan</b>, the tuner scans until it locks onto a signal. Then it sets the application's event handle. To resume scanning for the next valid signal in original range of frequencies, the application can call <b>ResumeCurrentScan</b>.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

