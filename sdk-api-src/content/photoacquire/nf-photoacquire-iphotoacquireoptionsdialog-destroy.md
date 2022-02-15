---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.Destroy
title: IPhotoAcquireOptionsDialog::Destroy (photoacquire.h)
description: The Destroy method closes and destroys the modeless dialog box created with the Create method.
helpviewer_keywords: ["Destroy","Destroy method [Picture Acquisition]","Destroy method [Picture Acquisition]","IPhotoAcquireOptionsDialog interface","IPhotoAcquireOptionsDialog interface [Picture Acquisition]","Destroy method","IPhotoAcquireOptionsDialog.Destroy","IPhotoAcquireOptionsDialog::Destroy","IPhotoAcquireOptionsDialogDestroy","photoacquire/IPhotoAcquireOptionsDialog::Destroy","picacq.iphotoacquireoptionsdialog_destroy"]
old-location: picacq\iphotoacquireoptionsdialog_destroy.htm
tech.root: picacq
ms.assetid: 787e12e9-b134-416a-9191-5a2cc6a922fd
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [Picture Acquisition], Destroy method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, IPhotoAcquireOptionsDialog interface [Picture Acquisition],Destroy method, IPhotoAcquireOptionsDialog.Destroy, IPhotoAcquireOptionsDialog::Destroy, IPhotoAcquireOptionsDialogDestroy, photoacquire/IPhotoAcquireOptionsDialog::Destroy, picacq.iphotoacquireoptionsdialog_destroy
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
 - IPhotoAcquireOptionsDialog::Destroy
 - photoacquire/IPhotoAcquireOptionsDialog::Destroy
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
 - IPhotoAcquireOptionsDialog.Destroy
---

# IPhotoAcquireOptionsDialog::Destroy


## -description

The <code>Destroy</code> method closes and destroys the modeless dialog box created with the <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-create">Create</a> method.



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

If you destroy the parent window, the child window will automatically be destroyed.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireoptionsdialog">IPhotoAcquireOptionsDialog Interface</a>
