---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.Create
title: IPhotoAcquireOptionsDialog::Create (photoacquire.h)
description: The Create method creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.
helpviewer_keywords: ["Create","Create method [Picture Acquisition]","Create method [Picture Acquisition]","IPhotoAcquireOptionsDialog interface","IPhotoAcquireOptionsDialog interface [Picture Acquisition]","Create method","IPhotoAcquireOptionsDialog.Create","IPhotoAcquireOptionsDialog::Create","IPhotoAcquireOptionsDialogCreate","photoacquire/IPhotoAcquireOptionsDialog::Create","picacq.iphotoacquireoptionsdialog_create"]
old-location: picacq\iphotoacquireoptionsdialog_create.htm
tech.root: picacq
ms.assetid: 22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad
ms.date: 12/05/2018
ms.keywords: Create, Create method [Picture Acquisition], Create method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, IPhotoAcquireOptionsDialog interface [Picture Acquisition],Create method, IPhotoAcquireOptionsDialog.Create, IPhotoAcquireOptionsDialog::Create, IPhotoAcquireOptionsDialogCreate, photoacquire/IPhotoAcquireOptionsDialog::Create, picacq.iphotoacquireoptionsdialog_create
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
 - IPhotoAcquireOptionsDialog::Create
 - photoacquire/IPhotoAcquireOptionsDialog::Create
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
 - IPhotoAcquireOptionsDialog.Create
---

# IPhotoAcquireOptionsDialog::Create


## -description

The <code>Create</code> method creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.

## -parameters

### -param hWndParent [in]

Handle to the parent window.

### -param phWndDialog [out]

Specifies the created dialog box.

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

The <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-initialize">Initialize</a> method should be called prior to the <code>Create</code> method.

The parent window indicated by <i>hWndParent</i> provides <b>OK</b> and <b>Cancel</b> buttons to the new dialog box instance.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireoptionsdialog">IPhotoAcquireOptionsDialog Interface</a>