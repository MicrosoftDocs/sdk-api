---
UID: NN:tuner.ITuner
title: ITuner (tuner.h)
author: windows-sdk-content
description: The ITuner interface is implemented on the Microsoft BDA Network Provider filters.
old-location: mstv\ituner.htm
tech.root: mstv
ms.assetid: 1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuner, ITuner interface [Microsoft TV Technologies], ITuner interface [Microsoft TV Technologies],described, ITunerInterface, mstv.ituner, tuner/ITuner
ms.topic: interface
f1_keywords: 
 - "tuner/ITuner"
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
 - ITuner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuner interface


## -description



The <b>ITuner</b> interface is implemented on the Microsoft <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filters. It provides methods for passing tune requests down to the hardware device and receiving current tuning settings. Generally, applications should use the derived interface <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> instead of <b>ITuner</b>.

<div class="alert"><b>Note</b>  Only applications that are intended to run on Windows 2000 should use this interface. Starting in Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuner</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-enumtuningspaces">EnumTuningSpaces</a>
</td>
<td align="left" width="63%">
Creates a collection of the tuning spaces preferred by this implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-get_preferredcomponenttypes">get_PreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Gets the collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects used for default component selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-get_signalstrength">get_SignalStrength</a>
</td>
<td align="left" width="63%">
Retrieves the Network Provider-specific signal strength metric.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-get_tunerequest">get_TuneRequest</a>
</td>
<td align="left" width="63%">
Gets the tune request currently in effect for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-get_tuningspace">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Gets the tuning space currently in effect for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_preferredcomponenttypes">put_PreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Sets the collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a> objects used for default component selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">put_TuneRequest</a>
</td>
<td align="left" width="63%">
Sets the tune request for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tuningspace">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Sets the tuning space for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-triggersignalevents">TriggerSignalEvents</a>
</td>
<td align="left" width="63%">
Enables the tuner to raise an event when the status of the signal changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-validate">Validate</a>
</td>
<td align="left" width="63%">
Returns a value indicating that the tune request can be carried out.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuner)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

