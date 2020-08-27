---
UID: NL:shidfact.CItemIDFactory
title: CItemIDFactory (shidfact.h)
description: Exposes methods for interacting with Shell data sources.
helpviewer_keywords: ["CItemIDFactory","CItemIDFactory class [Windows Shell]","CItemIDFactory class [Windows Shell]","described","shell.citemidfactory","shidfact/CItemIDFactory"]
old-location: shell\citemidfactory.htm
tech.root: shell
ms.assetid: 8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7
ms.date: 12/05/2018
ms.keywords: CItemIDFactory, CItemIDFactory class [Windows Shell], CItemIDFactory class [Windows Shell],described, shell.citemidfactory, shidfact/CItemIDFactory
f1_keywords:
- shidfact/CItemIDFactory
dev_langs:
- c++
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- shidfact.h
api_name:
- CItemIDFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CItemIDFactory class


## -description


Exposes methods for interacting with Shell data sources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CItemIDFactory</b> class inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder">IDelegateFolder</a>. <b>CItemIDFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>CItemIDFactory</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-createitemid">CreateItemID</a>
</td>
<td align="left" width="63%">
Creates an ItemID from the supplied data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-getdatafromidlist(pcuidlist_relative)">GetDataFromIDList</a>
</td>
<td align="left" width="63%">
Gets a read only pointer to the client provided structure in the first ItemID in the IDList.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh289343(v=vs.85)">GetPropertyFromIDList</a>
</td>
<td align="left" width="63%">Overloaded. Returns a property from the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> within the IDList.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-getpropertystorage">GetPropertyStorage</a>
</td>
<td align="left" width="63%">
Gets  a read only pointer to the serialized property storage that is used for storing metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-getpropertystoragefromidlist">GetPropertyStorageFromIDList</a>
</td>
<td align="left" width="63%">
create an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> based on the serialized property storage associated with the first ItemID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-isdelegatefolder">IsDelegateFolder</a>
</td>
<td align="left" width="63%">
Gets a Boolean value specifying whether the factory is a delegate folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shidfact/nf-shidfact-citemidfactory-setitemalloc">SetItemAlloc</a>
</td>
<td align="left" width="63%">
Provides the <b>CItemIDFactory</b> an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface used to allocate and free item IDs.

</td>
</tr>
</table> 


## -remarks



it is recomended that all data sources use this as it manages an important issue of security when  dealing with IDList parsing.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder">IDelegateFolder</a>
 

 

