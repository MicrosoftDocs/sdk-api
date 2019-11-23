---
UID: NN:wcmconfig.ISettingsItem
title: ISettingsItem (wcmconfig.h)

description: Navigates the settings tree, retrieves the metadata for a particular setting, and retrieves or modify its value.
old-location: smi\isettingsitem.htm
tech.root: SMI
ms.assetid: a743d942-69f9-426b-be88-adf88b9bb1e0

ms.date: 12/05/2018
ms.keywords: ISettingsItem, ISettingsItem interface [SMI], ISettingsItem interface [SMI],described, smi.isettingsitem, wcmconfig/ISettingsItem
ms.topic: interface
f1_keywords: 
 - "wcmconfig/ISettingsItem"
dev_langs:
 - c++
req.header: wcmconfig.h
req.include-header: 
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
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsItem interface


## -description


Navigates the settings tree, retrieves the metadata for a particular setting, and retrieves or modify its value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsItem</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-attributes">Attributes</a>
</td>
<td align="left" width="63%">
Gets a collection of the item attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-children">Children</a>
</td>
<td align="left" width="63%">
Gets a collection of the items children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-createlistelement">CreateListElement</a>
</td>
<td align="left" width="63%">
Creates a list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-createsettingbypath">CreateSettingByPath</a>
</td>
<td align="left" width="63%">
Creates a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets an attribute from the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getchild">GetChild</a>
</td>
<td align="left" width="63%">
Gets a child of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getdatatype">GetDataType</a>
</td>
<td align="left" width="63%">
Gets the data type of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getkeyvalue">GetKeyValue</a>
</td>
<td align="left" width="63%">
Extracts key values for any list that already exists in the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getlistkeyinformation">GetListKeyInformation</a>
</td>
<td align="left" width="63%">
Gets the list key information for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the item name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Gets the path information for an item. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestriction">GetRestriction</a>
</td>
<td align="left" width="63%">
Gets the information for a given restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestrictionfacets">GetRestrictionFacets</a>
</td>
<td align="left" width="63%">
Gets the restrictions defined on an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getsettingbypath">GetSettingByPath</a>
</td>
<td align="left" width="63%">
Gets a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getsettingtype">GetSettingType</a>
</td>
<td align="left" width="63%">
Gets the setting type of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets the item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getvalueraw">GetValueRaw</a>
</td>
<td align="left" width="63%">
Gets the value, as a byte array, of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-haschild">HasChild</a>
</td>
<td align="left" width="63%">
Determines if the item has children.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-removelistelement">RemoveListElement</a>
</td>
<td align="left" width="63%">
Removes a list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-removesettingbypath">RemoveSettingByPath</a>
</td>
<td align="left" width="63%">
Removes a child setting or list element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-setvalueraw">SetValueRaw</a>
</td>
<td align="left" width="63%">
Sets the value of an item.

</td>
</tr>
</table> 

