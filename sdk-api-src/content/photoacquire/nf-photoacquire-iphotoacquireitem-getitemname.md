---
UID: NF:photoacquire.IPhotoAcquireItem.GetItemName
title: IPhotoAcquireItem::GetItemName (photoacquire.h)
description: The GetItemName method retrieves the file name for an item.
helpviewer_keywords: ["GetItemName","GetItemName method [Picture Acquisition]","GetItemName method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","GetItemName method","IPhotoAcquireItem.GetItemName","IPhotoAcquireItem::GetItemName","IPhotoAcquireItemGetItemName","photoacquire/IPhotoAcquireItem::GetItemName","picacq.iphotoacquireitem_getitemname"]
old-location: picacq\iphotoacquireitem_getitemname.htm
tech.root: picacq
ms.assetid: 10048853-424b-4761-8a80-b1f674f856f4
ms.date: 12/05/2018
ms.keywords: GetItemName, GetItemName method [Picture Acquisition], GetItemName method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetItemName method, IPhotoAcquireItem.GetItemName, IPhotoAcquireItem::GetItemName, IPhotoAcquireItemGetItemName, photoacquire/IPhotoAcquireItem::GetItemName, picacq.iphotoacquireitem_getitemname
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
 - IPhotoAcquireItem::GetItemName
 - photoacquire/IPhotoAcquireItem::GetItemName
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
 - IPhotoAcquireItem.GetItemName
---

# IPhotoAcquireItem::GetItemName


## -description

The <code>GetItemName</code> method retrieves the file name for an item.

## -parameters

### -param pbstrItemName [out]

Pointer to a string containing the name of the item.

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

The file name consists of the display name and the extension, even if the <b>Hide extensions for known file types</b> setting is checked in the Windows <b>Folder Options</b> dialog box.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>