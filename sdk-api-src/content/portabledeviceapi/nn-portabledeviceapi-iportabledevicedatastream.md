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

# IPortableDeviceDataStream interface


## -description



The <b>IPortableDeviceDataStream</b> interface exposes additional methods on an <b>IStream</b> that is used for data transfers. It is obtained by calling <b>QueryInterface</b> on the <b>IStream</b> that is retrieved by <a href="https://msdn.microsoft.com/d5c9a85a-59fa-4b7b-acc7-d450ecd10593">IPortableDeviceResources::GetStream</a> or <a href="https://msdn.microsoft.com/ea3445cc-69af-40a6-a5a4-695e0f2e1fb6">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceDataStream</b> interface inherits from <b>IStream</b>. <b>IPortableDeviceDataStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceDataStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a call in progress on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd506e52-723d-4a3c-b73e-425700ccd3ec">GetObjectID</a>
</td>
<td align="left" width="63%">
Retrieves the object ID of the resource that was written to the device.

</td>
</tr>
</table> 

