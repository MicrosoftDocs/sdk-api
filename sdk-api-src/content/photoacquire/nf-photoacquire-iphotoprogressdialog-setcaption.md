---
UID: NF:photoacquire.IPhotoProgressDialog.SetCaption
title: IPhotoProgressDialog::SetCaption (photoacquire.h)
description: Sets the caption of the progress dialog box.
helpviewer_keywords: ["IPhotoProgressDialog interface [Picture Acquisition]","SetCaption method","IPhotoProgressDialog.SetCaption","IPhotoProgressDialog::SetCaption","IPhotoProgressDialogSetCaption","SetCaption","SetCaption method [Picture Acquisition]","SetCaption method [Picture Acquisition]","IPhotoProgressDialog interface","photoacquire/IPhotoProgressDialog::SetCaption","picacq.iphotoprogressdialog_setcaption"]
old-location: picacq\iphotoprogressdialog_setcaption.htm
tech.root: picacq
ms.assetid: 01689aa9-e3ae-48b4-b105-25880097a112
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetCaption method, IPhotoProgressDialog.SetCaption, IPhotoProgressDialog::SetCaption, IPhotoProgressDialogSetCaption, SetCaption, SetCaption method [Picture Acquisition], SetCaption method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetCaption, picacq.iphotoprogressdialog_setcaption
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
 - IPhotoProgressDialog::SetCaption
 - photoacquire/IPhotoProgressDialog::SetCaption
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
 - IPhotoProgressDialog.SetCaption
---

# IPhotoProgressDialog::SetCaption


## -description

Sets the caption of the progress dialog box.

## -parameters

### -param pszTitle [in]

Pointer to a null-terminated string containing the title of the progress dialog box.

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

The caption text is displayed above the progress indicator bar in the dialog box.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>