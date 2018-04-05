---
UID: NN:tuner.ITuner
title: ITuner
author: windows-driver-content
description: The ITuner interface is implemented on the Microsoft BDA Network Provider filters.
old-location: mstv\ituner.htm
old-project: mstv
ms.assetid: 1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITuner, ITuner interface [Microsoft TV Technologies], ITuner interface [Microsoft TV Technologies], described, ITunerInterface, mstv.ituner, tuner/ITuner
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
-	ITuner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuner interface


## -description



The <b>ITuner</b> interface is implemented on the Microsoft <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a> filters. It provides methods for passing tune requests down to the hardware device and receiving current tuning settings. Generally, applications should use the derived interface <a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner</a> instead of <b>ITuner</b>.

<div class="alert"><b>Note</b>  Only applications that are intended to run on Windows 2000 should use this interface. Starting in Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuner</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITuner</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6bd42b1b-b644-4fd7-9875-21a8d0f01243">EnumTuningSpaces</a>
</td>
<td align="left" width="63%">
Creates a collection of the tuning spaces preferred by this implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ed2d1b5-8ba3-4230-8cc3-f8207635a78a">get_PreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Gets the collection of <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects used for default component selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3040f56b-2c60-43c8-81b8-5c3538db08db">get_SignalStrength</a>
</td>
<td align="left" width="63%">
Retrieves the Network Provider-specific signal strength metric.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45967073-2e09-4490-967f-4ed3c9ed1d7e">get_TuneRequest</a>
</td>
<td align="left" width="63%">
Gets the tune request currently in effect for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01b6a280-d489-4b4f-ae87-17c9b9bb2838">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Gets the tuning space currently in effect for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cca12a71-c842-4340-9233-f4143f6e0eea">put_PreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Sets the collection of <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> objects used for default component selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69f71855-86d0-4ef9-a168-14e79461ec98">put_TuneRequest</a>
</td>
<td align="left" width="63%">
Sets the tune request for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae764317-3441-4abb-90e8-f7720cdfd957">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Sets the tuning space for the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cff8ee2-d474-4ea5-a284-608eb0288c9f">TriggerSignalEvents</a>
</td>
<td align="left" width="63%">
Enables the tuner to raise an event when the status of the signal changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10b238b1-1c71-4104-8c2d-f8446f0a3466">Validate</a>
</td>
<td align="left" width="63%">
Returns a value indicating that the tune request can be carried out.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuner)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

