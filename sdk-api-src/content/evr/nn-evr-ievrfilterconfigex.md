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

# IEVRFilterConfigEx interface


## -description


Configures the DirectShow <a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer</a> (EVR) filter.  To get a pointer to this interface, call <b>QueryInterface</b> on the  EVR filter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEVRFilterConfigEx</b> interface inherits from <a href="https://msdn.microsoft.com/13086d85-3dbf-4e9f-b065-d95e16412832">IEVRFilterConfig</a>. <b>IEVRFilterConfigEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEVRFilterConfigEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b286b77-de5f-44ce-82f4-d11a76fe2c4d">GetConfigPrefs</a>
</td>
<td align="left" width="63%">
Gets the configuration parameters for the  DirectShow EVR filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a565c7a-a8d7-433b-b454-262661c2c084">SetConfigPrefs</a>
</td>
<td align="left" width="63%">
Sets the configuration parameters for the DirectShow EVR filter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ead99cb3-2be2-42c6-ac22-be0c2ddf28d5">Enhanced Video Renderer Filter</a>



<a href="https://msdn.microsoft.com/13086d85-3dbf-4e9f-b065-d95e16412832">IEVRFilterConfig</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/3617adf2-ed7b-4788-abce-58bc22a14511">Video Quality Management</a>
 

 

