---
UID: NN:xamlom.IVisualTreeService
title: IVisualTreeService (xamlom.h)
description: Provides methods to manage a XAML visual tree.
old-location: xaml_diagnostics\ivisualtreeservice.htm
tech.root: xaml_diagnostics
ms.assetid: 5C0896E4-E37E-49DF-B303-1814BCA6F5B3
ms.date: 12/05/2018
ms.keywords: IVisualTreeService, IVisualTreeService interface, IVisualTreeService interface,described, xaml_diagnostics.ivisualtreeservice, xamlom/IVisualTreeService
f1_keywords:
- xamlom/IVisualTreeService
dev_langs:
- c++
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xamlom.h
api_name:
- IVisualTreeService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVisualTreeService interface


## -description


Provides methods to manage a XAML visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVisualTreeService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVisualTreeService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVisualTreeService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-addchild">AddChild</a>
</td>
<td align="left" width="63%">
Adds a child element to the collection at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-advisevisualtreechange">AdviseVisualTreeChange</a>
</td>
<td align="left" width="63%">
Starts listening for changes to the visual tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-clearchildren">ClearChildren</a>
</td>
<td align="left" width="63%">
Clears all child elements from the parent collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-clearproperty">ClearProperty</a>
</td>
<td align="left" width="63%">
Clears the specified property on a XAML element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of any XAML runtime, enum, or primitive type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-getcollectioncount">GetCollectionCount</a>
</td>
<td align="left" width="63%">
Gets the count of a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-getcollectionelements">GetCollectionElements</a>
</td>
<td align="left" width="63%">
Gets the elements in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-getenums">GetEnums</a>
</td>
<td align="left" width="63%">
Gets an array of all the enums defined in the XAML runtime and the total
    count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-getpropertyvalueschain">GetPropertyValuesChain</a>
</td>
<td align="left" width="63%">
Gets an array of all the
    properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-removechild">RemoveChild</a>
</td>
<td align="left" width="63%">
Removes the child element from the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property value on a XAML element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-unadvisevisualtreechange">UnadviseVisualTreeChange</a>
</td>
<td align="left" width="63%">
Stops listening for changes to the visual tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

