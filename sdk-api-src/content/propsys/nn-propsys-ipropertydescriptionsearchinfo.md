---
UID: NN:propsys.IPropertyDescriptionSearchInfo
title: IPropertyDescriptionSearchInfo (propsys.h)
description: Exposes search-related information for a property.helpviewer_keywords: ["IPropertyDescriptionSearchInfo","IPropertyDescriptionSearchInfo interface [Windows Properties]","IPropertyDescriptionSearchInfo interface [Windows Properties]","described","_shell_IPropertyDescriptionSearchInfo","properties.IPropertyDescriptionSearchInfo","propsys/IPropertyDescriptionSearchInfo","shell.IPropertyDescriptionSearchInfo"]
old-location: properties\IPropertyDescriptionSearchInfo.htm
tech.root: properties
ms.assetid: 7bd4be80-7459-4c3d-9da4-0580995e6db6
ms.date: 12/05/2018
ms.keywords: IPropertyDescriptionSearchInfo, IPropertyDescriptionSearchInfo interface [Windows Properties], IPropertyDescriptionSearchInfo interface [Windows Properties],described, _shell_IPropertyDescriptionSearchInfo, properties.IPropertyDescriptionSearchInfo, propsys/IPropertyDescriptionSearchInfo, shell.IPropertyDescriptionSearchInfo
f1_keywords:
- propsys/IPropertyDescriptionSearchInfo
dev_langs:
- c++
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
- Propsys.h
api_name:
- IPropertyDescriptionSearchInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyDescriptionSearchInfo interface


## -description


Exposes search-related information for a property. The information provided by this interface comes from the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-propertydescription">propertyDescription</a> schema, <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a> element for a given property. This information is used by the Windows Search Indexer. Most calling applications will not need to call this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionSearchInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyDescriptionSearchInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescriptionSearchInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionsearchinfo-getcolumnindextype">GetColumnIndexType</a>
</td>
<td align="left" width="63%">
Determines the how the current property is indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionsearchinfo-getmaxsize">GetMaxSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size value from the property schema's <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a> element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionsearchinfo-getprojectionstring">GetProjectionString</a>
</td>
<td align="left" width="63%">
Returns a pointer to a string containing the canonical name of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionsearchinfo-getsearchinfoflags">GetSearchInfoFlags</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-propdesc_searchinfo_flags">PROPDESC_SEARCHINFO_FLAGS</a> associated with the property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-propertydescription">propertyDescription</a>



<a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a>
 

 

