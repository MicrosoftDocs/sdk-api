---
UID: NN:tuner.IScanningTuner
title: IScanningTuner
author: windows-driver-content
description: The IScanningTuner interface is implemented on the BDA Network Provider filter.
old-location: mstv\iscanningtuner.htm
old-project: mstv
ms.assetid: faa99b87-ddbb-4e38-8681-bd5c8c4f81f3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IScanningTuner, IScanningTuner interface [Microsoft TV Technologies], IScanningTuner interface [Microsoft TV Technologies],described, IScanningTunerInterface, mstv.iscanningtuner, tuner/IScanningTuner
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IScanningTuner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTuner interface


## -description



The <b>IScanningTuner</b> interface is implemented on the <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a> filter. It inherits from <a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner</a> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="https://msdn.microsoft.com/ae764317-3441-4abb-90e8-f7720cdfd957">ITuner::put_TuningSpace</a> or <a href="https://msdn.microsoft.com/69f71855-86d0-4ef9-a168-14e79461ec98">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> outbound interface.

<div class="alert"><b>Note</b>  Only applications intended to run on Microsoft® Windows® 98 or Windows 2000 should use this interface. On Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScanningTuner</b> interface inherits from <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">ITuner</a>. <b>IScanningTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScanningTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98d1b484-13e7-4eeb-9e0c-a1215712bdc8">AutoProgram</a>
</td>
<td align="left" width="63%">
Scans for all channels with valid programming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e9120be-9f8c-442e-8253-812b2917f902">ScanDown</a>
</td>
<td align="left" width="63%">
Changes the channel to the next lower channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fa4d316-9f92-47d6-962f-ffe5c7e90a28">ScanUp</a>
</td>
<td align="left" width="63%">
Changes the channel to the next higher channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef78bae1-238f-4774-ab9a-b3681ba53656">SeekDown</a>
</td>
<td align="left" width="63%">
Changes the channel to the next lower channel with valid programming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43588b31-cac0-44c4-a282-b5939fed4ce7">SeekUp</a>
</td>
<td align="left" width="63%">
Changes the channel to the next higher channel with valid programming.

</td>
</tr>
</table> 


## -remarks



Currently the DVB-C and DVB-S Network Provider filters do not implement this interface. The interface is implemented for DVB-T.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTuner)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">ITuner</a>
 

 

