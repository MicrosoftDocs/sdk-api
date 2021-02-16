---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.DoModal
title: IPhotoAcquireOptionsDialog::DoModal (photoacquire.h)
description: The DoModal method creates and displays the options dialog box as a modal dialog box.
helpviewer_keywords: ["DoModal","DoModal method [Picture Acquisition]","DoModal method [Picture Acquisition]","IPhotoAcquireOptionsDialog interface","IPhotoAcquireOptionsDialog interface [Picture Acquisition]","DoModal method","IPhotoAcquireOptionsDialog.DoModal","IPhotoAcquireOptionsDialog::DoModal","IPhotoAcquireOptionsDialogDoModal","photoacquire/IPhotoAcquireOptionsDialog::DoModal","picacq.iphotoacquireoptionsdialog_domodal"]
old-location: picacq\iphotoacquireoptionsdialog_domodal.htm
tech.root: picacq
ms.assetid: fbceebc3-10dd-4028-9672-1976a459cafe
ms.date: 12/05/2018
ms.keywords: DoModal, DoModal method [Picture Acquisition], DoModal method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, IPhotoAcquireOptionsDialog interface [Picture Acquisition],DoModal method, IPhotoAcquireOptionsDialog.DoModal, IPhotoAcquireOptionsDialog::DoModal, IPhotoAcquireOptionsDialogDoModal, photoacquire/IPhotoAcquireOptionsDialog::DoModal, picacq.iphotoacquireoptionsdialog_domodal
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
 - IPhotoAcquireOptionsDialog::DoModal
 - photoacquire/IPhotoAcquireOptionsDialog::DoModal
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
 - IPhotoAcquireOptionsDialog.DoModal
---

# IPhotoAcquireOptionsDialog::DoModal


## -description

The <code>DoModal</code> method creates and displays the options dialog box as a modal dialog box.

## -parameters

### -param hWndParent [in]

Handle to the dialog's parent window.

### -param ppnReturnCode [out]

Specifies the code returned when the window is closed.

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

The modal dialog displayed by <b>DoModal</b> will have <b>OK</b> and <b>Cancel</b> buttons, whereas the <b>OK</b> and <b>Cancel</b> buttons of the modeless dialog displayed by <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-create">Create</a> must be provided by the parent window.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireoptionsdialog">IPhotoAcquireOptionsDialog Interface</a>