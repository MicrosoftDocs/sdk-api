---
UID: NF:photoacquire.IPhotoProgressDialog.SetPercentComplete
title: IPhotoProgressDialog::SetPercentComplete (photoacquire.h)
description: The SetPercentComplete method sets a value indicating the completed portion of the current operation.
helpviewer_keywords: ["IPhotoProgressDialog interface [Picture Acquisition]","SetPercentComplete method","IPhotoProgressDialog.SetPercentComplete","IPhotoProgressDialog::SetPercentComplete","IPhotoProgressDialogSetPercentComplete","SetPercentComplete","SetPercentComplete method [Picture Acquisition]","SetPercentComplete method [Picture Acquisition]","IPhotoProgressDialog interface","photoacquire/IPhotoProgressDialog::SetPercentComplete","picacq.iphotoprogressdialog_setpercentcomplete"]
old-location: picacq\iphotoprogressdialog_setpercentcomplete.htm
tech.root: picacq
ms.assetid: b2fb225d-6d2b-49f7-bbc9-715107e90df2
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetPercentComplete method, IPhotoProgressDialog.SetPercentComplete, IPhotoProgressDialog::SetPercentComplete, IPhotoProgressDialogSetPercentComplete, SetPercentComplete, SetPercentComplete method [Picture Acquisition], SetPercentComplete method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetPercentComplete, picacq.iphotoprogressdialog_setpercentcomplete
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
 - IPhotoProgressDialog::SetPercentComplete
 - photoacquire/IPhotoProgressDialog::SetPercentComplete
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
 - IPhotoProgressDialog.SetPercentComplete
---

# IPhotoProgressDialog::SetPercentComplete


## -description

The <code>SetPercentComplete</code> method sets a value indicating the completed portion of the current operation.

## -parameters

### -param nPercent [in]

Integer value indicating the percentage of the operation that has completed. This value may be between 0 and 100 only.

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

If you pass PROGRESS_INDETERMINATE to <code>SetPercentComplete</code>, the progress bar will not progress from left to right (from 0 to 100%), but will instead animate to indicate that an operation with an indeterminate end is taking place.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>