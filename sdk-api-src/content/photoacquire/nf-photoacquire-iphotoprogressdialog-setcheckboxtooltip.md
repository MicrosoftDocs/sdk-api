---
UID: NF:photoacquire.IPhotoProgressDialog.SetCheckboxTooltip
title: IPhotoProgressDialog::SetCheckboxTooltip (photoacquire.h)
description: The SetCheckboxTooltip method sets the tooltip text for the check box in the progress dialog box.
helpviewer_keywords: ["IPhotoProgressDialog interface [Picture Acquisition]","SetCheckboxTooltip method","IPhotoProgressDialog.SetCheckboxTooltip","IPhotoProgressDialog::SetCheckboxTooltip","IPhotoProgressDialogSetCheckboxTooltip","SetCheckboxTooltip","SetCheckboxTooltip method [Picture Acquisition]","SetCheckboxTooltip method [Picture Acquisition]","IPhotoProgressDialog interface","photoacquire/IPhotoProgressDialog::SetCheckboxTooltip","picacq.iphotoprogressdialog_setcheckboxtooltip"]
old-location: picacq\iphotoprogressdialog_setcheckboxtooltip.htm
tech.root: picacq
ms.assetid: 88719891-9661-4766-adce-6b74cf9a87ef
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],SetCheckboxTooltip method, IPhotoProgressDialog.SetCheckboxTooltip, IPhotoProgressDialog::SetCheckboxTooltip, IPhotoProgressDialogSetCheckboxTooltip, SetCheckboxTooltip, SetCheckboxTooltip method [Picture Acquisition], SetCheckboxTooltip method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::SetCheckboxTooltip, picacq.iphotoprogressdialog_setcheckboxtooltip
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
 - IPhotoProgressDialog::SetCheckboxTooltip
 - photoacquire/IPhotoProgressDialog::SetCheckboxTooltip
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
 - IPhotoProgressDialog.SetCheckboxTooltip
---

# IPhotoProgressDialog::SetCheckboxTooltip


## -description

The <code>SetCheckboxTooltip</code> method sets the tooltip text for the check box in the progress dialog box.

## -parameters

### -param nCheckboxId [in]

Integer containing the check box identifier (ID).

### -param pszCheckboxTooltipText [in]

Pointer to a null-terminated string containing the check box tooltip text.

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