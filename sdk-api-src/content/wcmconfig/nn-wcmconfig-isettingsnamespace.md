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

# ISettingsNamespace interface


## -description


Performs operations to set, retrieve, and validate settings, and save changes for a namespace instance.

To retrieve an <b>ISettingsNamespace</b> interface pointer, call the <a href="https://msdn.microsoft.com/4f8193f5-9e9f-4819-aa2e-72b8623eca71">ISettingsEngine::GetNamespace</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsNamespace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsNamespace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsNamespace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/804cab32-eb0a-4e6e-8f58-042c1f5dde77">CreateSettingByPath</a>
</td>
<td align="left" width="63%">
Creates a setting object specified by its path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0623114-8f25-4870-a1c7-4f4e3ecf0348">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets the value of an attribute of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546831">GetIdentity</a>
</td>
<td align="left" width="63%">
Retrieves the identity of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7deadfed-036d-40cd-88b6-7afaf8fc7d41">GetSettingByPath</a>
</td>
<td align="left" width="63%">
Retrieves a  setting by specifying its path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c2cf0be-9c9f-46d6-9108-47d2ad405645">RemoveSettingByPath</a>
</td>
<td align="left" width="63%">
Removes the setting object specified by a path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Updates the settings namespace to persistent and visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt168438">Settings</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the top-level settings for the namespace.

</td>
</tr>
</table> 

