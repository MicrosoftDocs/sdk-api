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

# IActivatableClassRegistration interface


## -description


Enables getting  the registration info for a class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivatableClassRegistration</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IActivatableClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivatableClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AE55B74-8AC3-4F13-8FEE-7C3C52DEE96F">ActivatableClassId</a>
</td>
<td align="left" width="63%">
Gets the class identifier for the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/145DF7F2-839A-4B94-B4DC-BA2103A04D2F">ActivationType</a>
</td>
<td align="left" width="63%">
Gets the kind of activation for the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E058C71F-5F37-4089-89BD-28D8FF7E0711">Attributes</a>
</td>
<td align="left" width="63%">
Gets the attributes associated with the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3DFE773C-CF63-489A-988B-2FFF4215C8BF">RegisteredTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ACA72E3B-E559-4BE8-894F-A4D5F1FF3742">RegistrationScope</a>
</td>
<td align="left" width="63%">
Gets the deployment scope of the current activatable class.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/00E9476E-45E0-4D97-9DA4-FD293674BED4">IDllServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a>
 

 

