---
UID: NF:photoacquire.IPhotoProgressDialog.ShowCheckbox
title: IPhotoProgressDialog::ShowCheckbox (photoacquire.h)
description: The ShowCheckbox method indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.
helpviewer_keywords: ["IPhotoProgressDialog interface [Picture Acquisition]","ShowCheckbox method","IPhotoProgressDialog.ShowCheckbox","IPhotoProgressDialog::ShowCheckbox","IPhotoProgressDialogShowCheckbox","ShowCheckbox","ShowCheckbox method [Picture Acquisition]","ShowCheckbox method [Picture Acquisition]","IPhotoProgressDialog interface","photoacquire/IPhotoProgressDialog::ShowCheckbox","picacq.iphotoprogressdialog_showcheckbox"]
old-location: picacq\iphotoprogressdialog_showcheckbox.htm
tech.root: picacq
ms.assetid: 6518c073-b4d9-49df-819f-473028ad230a
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],ShowCheckbox method, IPhotoProgressDialog.ShowCheckbox, IPhotoProgressDialog::ShowCheckbox, IPhotoProgressDialogShowCheckbox, ShowCheckbox, ShowCheckbox method [Picture Acquisition], ShowCheckbox method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::ShowCheckbox, picacq.iphotoprogressdialog_showcheckbox
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
 - IPhotoProgressDialog::ShowCheckbox
 - photoacquire/IPhotoProgressDialog::ShowCheckbox
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
 - IPhotoProgressDialog.ShowCheckbox
---

# IPhotoProgressDialog::ShowCheckbox


## -description

The <code>ShowCheckbox</code> method indicates whether to show the check box in the progress dialog box indicating whether to delete images after transfer.

## -parameters

### -param nCheckboxId [in]

Integer containing the check box identifier (ID).

### -param fShow [in]

Flag that, when set to <b>TRUE</b>, indicates that the check box will appear.

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

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>