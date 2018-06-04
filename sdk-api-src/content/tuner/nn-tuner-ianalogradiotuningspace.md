---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAnalogRadioTuningSpace interface


## -description



The <b>IAnalogRadioTuningSpace</b> interface provides methods for getting and setting parameters associated with tuning spaces for analog radio transmissions.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogRadioTuningSpace</b> interface inherits from <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>. <b>IAnalogRadioTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogRadioTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baf4fe54-6e8c-49a7-b99f-4efeb7c65757">get_MaxFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e26360b-b00b-4741-a3c6-814843ff93e7">get_MinFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the minimum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fed3a33-c37c-486d-8bd6-4b80252867e1">get_Step</a>
</td>
<td align="left" width="63%">
Retrieves the step increment for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c5c3d7b-820a-4741-8a3a-4c1ffd67870a">put_MaxFrequency</a>
</td>
<td align="left" width="63%">
Sets the maximum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a7bb5e8-ed21-4b3b-96eb-861aa77621ca">put_MinFrequency</a>
</td>
<td align="left" width="63%">
Sets the minimum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8e5075f-4d30-4c32-8041-7e60d7d82f8d">put_Step</a>
</td>
<td align="left" width="63%">
Sets the step increment for this tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogRadioTuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

