---
UID: NN:tuner.IScanningTunerEx
title: IScanningTunerEx
author: windows-sdk-content
description: This topic applies to Windows Vista.
old-location: mstv\iscanningtunerex.htm
old-project: mstv
ms.assetid: 3f89173a-d24b-400c-a229-28efb7a703be
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], IScanningTunerEx interface [Microsoft TV Technologies],described, IScanningTunerExInterface, mstv.iscanningtunerex, tuner/IScanningTunerEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IScanningTunerEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx interface


## -description



This topic applies to Windows Vista.
        

The <b>IScanningTunerEx</b> interface is an extended version of <a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner</a> and is exposed by the <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a> filter. It inherits from <b>IScanningTuner</b> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="https://msdn.microsoft.com/ae764317-3441-4abb-90e8-f7720cdfd957">ITuner::put_TuningSpace</a> or <a href="https://msdn.microsoft.com/69f71855-86d0-4ef9-a168-14e79461ec98">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> outbound interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScanningTunerEx</b> interface inherits from <a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner</a>. <b>IScanningTunerEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScanningTunerEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5237236-50f3-49dd-aec0-578e0a8430c2">GetCurrentLocator</a>
</td>
<td align="left" width="63%">
Retrieves the current locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a3edf23-d782-4bfb-84c2-33eab7cb9d19">GetCurrentTunerStandardCapability</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's capabilities for a specified broadcast standard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dc7aeec-2a9d-4dfb-9f67-36d8131cc130">GetTunerScanningCapability</a>
</td>
<td align="left" width="63%">
Retrieves the set of broadcast standards supported by the tuner and the tuner's scanning capability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e91f5ca-5a2e-414e-bf4c-882ba6a08b98">GetTunerStatus</a>
</td>
<td align="left" width="63%">
Returns the current status of the most recent call to <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>
</td>
<td align="left" width="63%">
Scans a range of frequencies until the tuner locks onto a signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d855ae4-a49c-43d6-9ba0-9f6158f4034f">ResumeCurrentScan</a>
</td>
<td align="left" width="63%">
Resumes scanning the range of frequencies specified in <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223a904a-1f15-4010-b25f-8551c1e9fc25">SetScanSignalTypeFilter</a>
</td>
<td align="left" width="63%">
Specifies the type of signal for which to scan.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ab18d8a-1e79-45c2-a8b6-9c27ecb68de2">TerminateCurrentScan</a>
</td>
<td align="left" width="63%">
Interrupts the current scan, if a scan is in progress.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTunerEx)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner</a>
 

 

