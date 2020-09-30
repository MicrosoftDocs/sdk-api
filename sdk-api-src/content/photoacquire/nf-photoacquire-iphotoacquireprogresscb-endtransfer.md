---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndTransfer
title: IPhotoAcquireProgressCB::EndTransfer (photoacquire.h)
description: The EndTransfer method provides extended functionality when the transfer of all files is complete. The application provides the implementation of the EndTransfer method.
helpviewer_keywords: ["EndTransfer","EndTransfer method [Picture Acquisition]","EndTransfer method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","EndTransfer method","IPhotoAcquireProgressCB.EndTransfer","IPhotoAcquireProgressCB::EndTransfer","IPhotoAcquireProgressCBEndTransfer","photoacquire/IPhotoAcquireProgressCB::EndTransfer","picacq.iphotoacquireprogresscb_endtransfer"]
old-location: picacq\iphotoacquireprogresscb_endtransfer.htm
tech.root: picacq
ms.assetid: 9e0fada0-6c83-4e82-a3ac-c5a4832f053f
ms.date: 12/05/2018
ms.keywords: EndTransfer, EndTransfer method [Picture Acquisition], EndTransfer method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],EndTransfer method, IPhotoAcquireProgressCB.EndTransfer, IPhotoAcquireProgressCB::EndTransfer, IPhotoAcquireProgressCBEndTransfer, photoacquire/IPhotoAcquireProgressCB::EndTransfer, picacq.iphotoacquireprogresscb_endtransfer
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
 - IPhotoAcquireProgressCB::EndTransfer
 - photoacquire/IPhotoAcquireProgressCB::EndTransfer
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
 - IPhotoAcquireProgressCB.EndTransfer
---

# IPhotoAcquireProgressCB::EndTransfer


## -description

The <code>EndTransfer</code> method provides extended functionality when the transfer of all files is complete. The application provides the implementation of the <code>EndTransfer</code> method.

## -parameters

### -param hr [in]

Specifies the result of the transfer.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not yet implemented

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>