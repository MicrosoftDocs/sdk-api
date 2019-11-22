---
UID: NN:shobjidl_core.IRelatedItem
title: IRelatedItem (shobjidl_core.h)

description: Exposes methods that derive related items with specific relationships.
old-location: shell\IRelatedItem.htm
tech.root: shell
ms.assetid: f42d218c-0251-45e0-b05a-f1ccdcaf036c

ms.date: 12/05/2018
ms.keywords: IRelatedItem, IRelatedItem interface [Windows Shell], IRelatedItem interface [Windows Shell],described, _shell_IRelatedItem, shell.IRelatedItem, shobjidl_core/IRelatedItem
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IRelatedItem"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IRelatedItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRelatedItem interface


## -description


Exposes methods that derive related items with specific relationships.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRelatedItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRelatedItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRelatedItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irelateditem-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that is related to this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irelateditem-getitemidlist">GetItemIDList</a>
</td>
<td align="left" width="63%">
Gets the PIDL for the item that is related.

</td>
</tr>
</table> 


## -remarks



Do not implement this interface directly. This is a base interface (other interfaces derive from it) for a set of interfaces that describes the relationship between two items, (For example <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem">IDisplayItem</a>).  Do not query for this interface directly, for example, using <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a>. Instead, use the derived interfaces.

An example derivation is the creation of an identity name handler. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname">IIdentityName</a>. Other interfaces that may derive from this interface include <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem">ICurrentItem</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem">ITransferMediumItem</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler">IShellItem::BindToHandler</a>
 

 

