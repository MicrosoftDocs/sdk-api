---
UID: NF:photoacquire.IPhotoProgressDialog.Create
title: IPhotoProgressDialog::Create (photoacquire.h)
description: The Create method creates and displays a progress dialog box that can be shown during image enumeration and acquisition.
helpviewer_keywords: ["Create","Create method [Picture Acquisition]","Create method [Picture Acquisition]","IPhotoProgressDialog interface","IPhotoProgressDialog interface [Picture Acquisition]","Create method","IPhotoProgressDialog.Create","IPhotoProgressDialog::Create","IPhotoProgressDialogCreate","photoacquire/IPhotoProgressDialog::Create","picacq.iphotoprogressdialog_create"]
old-location: picacq\iphotoprogressdialog_create.htm
tech.root: picacq
ms.assetid: e68ac203-f97b-4459-b344-c845f0ac0f1b
ms.date: 12/05/2018
ms.keywords: Create, Create method [Picture Acquisition], Create method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],Create method, IPhotoProgressDialog.Create, IPhotoProgressDialog::Create, IPhotoProgressDialogCreate, photoacquire/IPhotoProgressDialog::Create, picacq.iphotoprogressdialog_create
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
 - IPhotoProgressDialog::Create
 - photoacquire/IPhotoProgressDialog::Create
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
 - IPhotoProgressDialog.Create
---

# IPhotoProgressDialog::Create


## -description

The <code>Create</code> method creates and displays a progress dialog box that can be shown during image enumeration and acquisition.

## -parameters

### -param hwndParent [in]

Handle of the parent window.

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

The dialog box that is created is modal, and runs in its own thread.

To close the dialog, call <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-destroy">Destroy</a>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-destroy">IPhotoProgressDialog::Destroy</a>