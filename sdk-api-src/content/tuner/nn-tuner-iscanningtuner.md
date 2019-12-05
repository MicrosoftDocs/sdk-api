---
UID: NN:tuner.IScanningTuner
title: IScanningTuner (tuner.h)
description: The IScanningTuner interface is implemented on the BDA Network Provider filter.
old-location: mstv\iscanningtuner.htm
tech.root: mstv
ms.assetid: faa99b87-ddbb-4e38-8681-bd5c8c4f81f3
ms.date: 12/05/2018
ms.keywords: IScanningTuner, IScanningTuner interface [Microsoft TV Technologies], IScanningTuner interface [Microsoft TV Technologies],described, IScanningTunerInterface, mstv.iscanningtuner, tuner/IScanningTuner
ms.topic: interface
f1_keywords:
- tuner/IScanningTuner
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
- tuner.h
api_name:
- IScanningTuner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScanningTuner interface


## -description



The <b>IScanningTuner</b> interface is implemented on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filter. It inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner</a> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tuningspace">ITuner::put_TuningSpace</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcastevent">IBroadcastEvent</a> outbound interface.

<div class="alert"><b>Note</b>  Only applications intended to run on Microsoft® Windows® 98 or Windows 2000 should use this interface. On Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScanningTuner</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">ITuner</a>. <b>IScanningTuner</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-autoprogram">AutoProgram</a>
</td>
<td align="left" width="63%">
Scans for all channels with valid programming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-scandown">ScanDown</a>
</td>
<td align="left" width="63%">
Changes the channel to the next lower channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-scanup">ScanUp</a>
</td>
<td align="left" width="63%">
Changes the channel to the next higher channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-seekdown">SeekDown</a>
</td>
<td align="left" width="63%">
Changes the channel to the next lower channel with valid programming.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtuner-seekup">SeekUp</a>
</td>
<td align="left" width="63%">
Changes the channel to the next higher channel with valid programming.

</td>
</tr>
</table> 


## -remarks



Currently the DVB-C and DVB-S Network Provider filters do not implement this interface. The interface is implemented for DVB-T.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTuner)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">ITuner</a>
 

 

