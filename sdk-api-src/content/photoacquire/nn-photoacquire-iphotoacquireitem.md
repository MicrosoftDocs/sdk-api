---
UID: NN:photoacquire.IPhotoAcquireItem
title: IPhotoAcquireItem (photoacquire.h)
description: The IPhotoAcquireItem interface provides methods for working with items as they are acquired from a device.
helpviewer_keywords: ["IPhotoAcquireItem","IPhotoAcquireItem interface [Picture Acquisition]","IPhotoAcquireItem interface [Picture Acquisition]","described","IPhotoAcquireItemInterface","photoacquire/IPhotoAcquireItem","picacq.iphotoacquireitem"]
old-location: picacq\iphotoacquireitem.htm
tech.root: acquisition
ms.assetid: 57e099eb-bf8d-4465-af4d-fcfc3eee3b5b
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireItem, IPhotoAcquireItem interface [Picture Acquisition], IPhotoAcquireItem interface [Picture Acquisition],described, IPhotoAcquireItemInterface, photoacquire/IPhotoAcquireItem, picacq.iphotoacquireitem
f1_keywords:
- photoacquire/IPhotoAcquireItem
dev_langs:
- c++
req.header: photoacquire.h
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
- photoacquire.h
api_name:
- IPhotoAcquireItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquireItem interface


## -description



The <code>IPhotoAcquireItem</code> interface provides methods for working with items as they are acquired from a device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-candelete">CanDelete</a>
</td>
<td align="left" width="63%">
Indicates whether an item may be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getitemname">GetItemName</a>
</td>
<td align="left" width="63%">
Retrieves the file name for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a read-only stream containing the contents of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getsubitemat">GetSubItemAt</a>
</td>
<td align="left" width="63%">
Retrieves the subitem of an item, given the index of the subitem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getsubitemcount">GetSubItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of subitems contained in an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getthumbnail">GetThumbnail</a>
</td>
<td align="left" width="63%">
Retrieves the thumbnail provided for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property for an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

