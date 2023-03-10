---
UID: NF:photoacquire.IPhotoProgressDialog.Destroy
title: IPhotoProgressDialog::Destroy (photoacquire.h)
description: The Destroy method closes and disposes of the progress dialog box shown during image enumeration and acquisition.
helpviewer_keywords: ["Destroy","Destroy method [Picture Acquisition]","Destroy method [Picture Acquisition]","IPhotoProgressDialog interface","IPhotoProgressDialog interface [Picture Acquisition]","Destroy method","IPhotoProgressDialog.Destroy","IPhotoProgressDialog::Destroy","IPhotoProgressDialogDestroy","photoacquire/IPhotoProgressDialog::Destroy","picacq.iphotoprogressdialog_destroy"]
old-location: picacq\iphotoprogressdialog_destroy.htm
tech.root: picacq
ms.assetid: 8690c67b-5f96-4e8c-8685-91fe5ed65511
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [Picture Acquisition], Destroy method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],Destroy method, IPhotoProgressDialog.Destroy, IPhotoProgressDialog::Destroy, IPhotoProgressDialogDestroy, photoacquire/IPhotoProgressDialog::Destroy, picacq.iphotoprogressdialog_destroy
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
 - IPhotoProgressDialog::Destroy
 - photoacquire/IPhotoProgressDialog::Destroy
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
 - IPhotoProgressDialog.Destroy
---

# IPhotoProgressDialog::Destroy


## -description

The <code>Destroy</code> method closes and disposes of the progress dialog box shown during image enumeration and acquisition.



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

Calling <code>Destroy</code> is the only way to close the progress dialog box. If <code>Destroy</code> is not called, the dialog box will remain open. The dialog box is not automatically closed when the operation in progress completes.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>
