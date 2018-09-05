---
UID: NN:wcmconfig.ISettingsItem
title: ISettingsItem
author: windows-sdk-content
description: Navigates the settings tree, retrieves the metadata for a particular setting, and retrieves or modify its value.
old-location: smi\isettingsitem.htm
old-project: SMI
ms.assetid: a743d942-69f9-426b-be88-adf88b9bb1e0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISettingsItem, ISettingsItem interface [SMI], ISettingsItem interface [SMI],described, smi.isettingsitem, wcmconfig/ISettingsItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wcmconfig.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem interface


## -description


Navigates the settings tree, retrieves the metadata for a particular setting, and retrieves or modify its value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a6751f2-0934-4329-9ab2-9ae9802bc33e">Attributes</a>
</td>
<td align="left" width="63%">
Gets a collection of the item attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33bd7f91-c414-420e-bc18-1114924b93e9">Children</a>
</td>
<td align="left" width="63%">
Gets a collection of the items children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c18fd849-aaa5-49d0-9e72-b3134a6f2be8">CreateListElement</a>
</td>
<td align="left" width="63%">
Creates a list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b51329e-dc81-46dc-b174-0191e2eea44a">CreateSettingByPath</a>
</td>
<td align="left" width="63%">
Creates a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/995184e4-05ff-41f1-9404-872a82bedd49">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets an attribute from the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a3d3212-bd47-46fb-9ce1-79ac109c6444">GetChild</a>
</td>
<td align="left" width="63%">
Gets a child of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ccb99aa-35d5-4f0b-a4f3-a42c4579bc4a">GetDataType</a>
</td>
<td align="left" width="63%">
Gets the data type of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a627d0aa-05ef-43b6-a8e8-bb0770dd8873">GetKeyValue</a>
</td>
<td align="left" width="63%">
Extracts key values for any list that already exists in the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34ee8457-34d1-4eff-813b-f59c35c4aa95">GetListKeyInformation</a>
</td>
<td align="left" width="63%">
Gets the list key information for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8517c53-5833-4087-91eb-3eb9301e0d3a">GetName</a>
</td>
<td align="left" width="63%">
Gets the item name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/221b5929-7300-4d01-b93e-7c82c446f52b">GetPath</a>
</td>
<td align="left" width="63%">
Gets the path information for an item. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14bc4956-e8ea-464b-949e-ddc7ae445c1a">GetRestriction</a>
</td>
<td align="left" width="63%">
Gets the information for a given restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64cf82d5-c210-4ff2-a7c8-1a284859382e">GetRestrictionFacets</a>
</td>
<td align="left" width="63%">
Gets the restrictions defined on an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4270c46-b214-4232-b414-d6b6e4e35635">GetSettingByPath</a>
</td>
<td align="left" width="63%">
Gets a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d222939f-9295-4751-8b32-586fa9930177">GetSettingType</a>
</td>
<td align="left" width="63%">
Gets the setting type of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11b61570-d1ed-4dcf-b533-873096ae80b9">GetValue</a>
</td>
<td align="left" width="63%">
Gets the item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b4b96df-1286-49be-869a-404adaead27a">GetValueRaw</a>
</td>
<td align="left" width="63%">
Gets the value, as a byte array, of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c22cb66-5116-4107-9fb0-a6a4161b6f8e">HasChild</a>
</td>
<td align="left" width="63%">
Determines if the item has children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dca22b5-b4e3-4bb6-9eb4-5507472b63b2">RemoveListElement</a>
</td>
<td align="left" width="63%">
Removes a list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5613df85-009f-4aab-91bc-797a6cf73cd0">RemoveSettingByPath</a>
</td>
<td align="left" width="63%">
Removes a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52b7e852-b389-47ec-a9d0-e4ce2e95f1f8">SetValue</a>
</td>
<td align="left" width="63%">
Sets the item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65925c16-7a12-440f-ba2d-9156e41049ba">SetValueRaw</a>
</td>
<td align="left" width="63%">
Sets the value of an item.

</td>
</tr>
</table> 

