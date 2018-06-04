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

# ISyncProviderConfigUIInfo interface


## -description


Represents the information and properties needed to create an instance of a synchronization provider configuration UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderConfigUIInfo</b> interface inherits from <b>IPropertyStore</b>. <b>ISyncProviderConfigUIInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProviderConfigUIInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb9a2f2f-4c9f-405c-90f6-b251ab1a652d">GetSyncProviderConfigUI</a>
</td>
<td align="left" width="63%">
Creates an instance of a synchronization provider configuration UI.

</td>
</tr>
</table> 


## -remarks



You can get and set the properties of a  synchronization provider configuration UI by calling the <a href="https://msdn.microsoft.com/eb9a2f2f-4c9f-405c-90f6-b251ab1a652d">GetSyncProviderConfigUI</a>
method and manipulating the configuration UI's <b>IPropertyStore</b>.




## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

