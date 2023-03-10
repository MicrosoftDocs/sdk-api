---
UID: NF:photoacquire.IPhotoAcquireItem.GetSubItemCount
title: IPhotoAcquireItem::GetSubItemCount (photoacquire.h)
description: The GetSubItemCount method retrieves the number of subitems contained in an item.
helpviewer_keywords: ["GetSubItemCount","GetSubItemCount method [Picture Acquisition]","GetSubItemCount method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","GetSubItemCount method","IPhotoAcquireItem.GetSubItemCount","IPhotoAcquireItem::GetSubItemCount","IPhotoAcquireItemGetSubItemCount","photoacquire/IPhotoAcquireItem::GetSubItemCount","picacq.iphotoacquireitem_getsubitemcount"]
old-location: picacq\iphotoacquireitem_getsubitemcount.htm
tech.root: picacq
ms.assetid: 2790d551-42ae-4009-998e-2579687203d6
ms.date: 12/05/2018
ms.keywords: GetSubItemCount, GetSubItemCount method [Picture Acquisition], GetSubItemCount method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetSubItemCount method, IPhotoAcquireItem.GetSubItemCount, IPhotoAcquireItem::GetSubItemCount, IPhotoAcquireItemGetSubItemCount, photoacquire/IPhotoAcquireItem::GetSubItemCount, picacq.iphotoacquireitem_getsubitemcount
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireItem::GetSubItemCount
 - photoacquire/IPhotoAcquireItem::GetSubItemCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireItem.GetSubItemCount
---

# IPhotoAcquireItem::GetSubItemCount


## -description

The <code>GetSubItemCount</code> method retrieves the number of subitems contained in an item.

## -parameters

### -param pnCount [out]

Pointer to an integer containing the count of subitems.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

If an error occurs, <i>pnCount</i> will be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>