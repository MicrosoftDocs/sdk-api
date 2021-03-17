---
UID: NF:photoacquire.IPhotoAcquireProgressCB.DirectoryCreated
title: IPhotoAcquireProgressCB::DirectoryCreated (photoacquire.h)
description: The DirectoryCreated method provides extended functionality when a destination directory is created during the acquisition process. The application provides the implementation of the DirectoryCreated method.
helpviewer_keywords: ["DirectoryCreated","DirectoryCreated method [Picture Acquisition]","DirectoryCreated method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","DirectoryCreated method","IPhotoAcquireProgressCB.DirectoryCreated","IPhotoAcquireProgressCB::DirectoryCreated","IPhotoAcquireProgressCBDirectoryCreated","photoacquire/IPhotoAcquireProgressCB::DirectoryCreated","picacq.iphotoacquireprogresscb_directorycreated"]
old-location: picacq\iphotoacquireprogresscb_directorycreated.htm
tech.root: picacq
ms.assetid: c784750c-3f73-4ebb-ad38-cc05aada0fca
ms.date: 12/05/2018
ms.keywords: DirectoryCreated, DirectoryCreated method [Picture Acquisition], DirectoryCreated method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],DirectoryCreated method, IPhotoAcquireProgressCB.DirectoryCreated, IPhotoAcquireProgressCB::DirectoryCreated, IPhotoAcquireProgressCBDirectoryCreated, photoacquire/IPhotoAcquireProgressCB::DirectoryCreated, picacq.iphotoacquireprogresscb_directorycreated
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
 - IPhotoAcquireProgressCB::DirectoryCreated
 - photoacquire/IPhotoAcquireProgressCB::DirectoryCreated
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
 - IPhotoAcquireProgressCB.DirectoryCreated
---

# IPhotoAcquireProgressCB::DirectoryCreated


## -description

The <code>DirectoryCreated</code> method provides extended functionality when a destination directory is created during the acquisition process. The application provides the implementation of the <code>DirectoryCreated</code> method.

## -parameters

### -param pszDirectory [in]

Pointer to a null-terminated string containing the directory.

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
The method is not yet implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>