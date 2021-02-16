---
UID: NF:photoacquire.IPhotoAcquireItem.GetStream
title: IPhotoAcquireItem::GetStream (photoacquire.h)
description: The GetStream method retrieves a read-only stream containing the contents of an item.
helpviewer_keywords: ["GetStream","GetStream method [Picture Acquisition]","GetStream method [Picture Acquisition]","IPhotoAcquireItem interface","IPhotoAcquireItem interface [Picture Acquisition]","GetStream method","IPhotoAcquireItem.GetStream","IPhotoAcquireItem::GetStream","IPhotoAcquireItemGetStream","photoacquire/IPhotoAcquireItem::GetStream","picacq.iphotoacquireitem_getstream"]
old-location: picacq\iphotoacquireitem_getstream.htm
tech.root: picacq
ms.assetid: d0b138aa-42df-4bb6-905d-647b2289df58
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [Picture Acquisition], GetStream method [Picture Acquisition],IPhotoAcquireItem interface, IPhotoAcquireItem interface [Picture Acquisition],GetStream method, IPhotoAcquireItem.GetStream, IPhotoAcquireItem::GetStream, IPhotoAcquireItemGetStream, photoacquire/IPhotoAcquireItem::GetStream, picacq.iphotoacquireitem_getstream
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
 - IPhotoAcquireItem::GetStream
 - photoacquire/IPhotoAcquireItem::GetStream
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
 - IPhotoAcquireItem.GetStream
---

# IPhotoAcquireItem::GetStream


## -description

The <code>GetStream</code> method retrieves a read-only stream containing the contents of an item.

## -parameters

### -param ppStream [out]

Returns a stream object with the file contents.

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

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem Interface</a>