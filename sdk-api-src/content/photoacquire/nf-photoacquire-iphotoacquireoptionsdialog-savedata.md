---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.SaveData
title: IPhotoAcquireOptionsDialog::SaveData (photoacquire.h)
description: The SaveData method saves acquisition settings from the options dialog box to the registry so that a subsequent instance of the dialog can be initialized with the same settings.
helpviewer_keywords: ["IPhotoAcquireOptionsDialog interface [Picture Acquisition]","SaveData method","IPhotoAcquireOptionsDialog.SaveData","IPhotoAcquireOptionsDialog::SaveData","IPhotoAcquireOptionsDialogSaveData","SaveData","SaveData method [Picture Acquisition]","SaveData method [Picture Acquisition]","IPhotoAcquireOptionsDialog interface","photoacquire/IPhotoAcquireOptionsDialog::SaveData","picacq.iphotoacquireoptionsdialog_savedata"]
old-location: picacq\iphotoacquireoptionsdialog_savedata.htm
tech.root: picacq
ms.assetid: 271c2bfb-67a9-4998-90d1-4ed61f89aa03
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireOptionsDialog interface [Picture Acquisition],SaveData method, IPhotoAcquireOptionsDialog.SaveData, IPhotoAcquireOptionsDialog::SaveData, IPhotoAcquireOptionsDialogSaveData, SaveData, SaveData method [Picture Acquisition], SaveData method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, photoacquire/IPhotoAcquireOptionsDialog::SaveData, picacq.iphotoacquireoptionsdialog_savedata
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
 - IPhotoAcquireOptionsDialog::SaveData
 - photoacquire/IPhotoAcquireOptionsDialog::SaveData
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
 - IPhotoAcquireOptionsDialog.SaveData
---

# IPhotoAcquireOptionsDialog::SaveData


## -description

The <code>SaveData</code> method saves acquisition settings from the options dialog box to the registry so that a subsequent instance of the dialog can be initialized with the same settings.



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

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireoptionsdialog">IPhotoAcquireOptionsDialog Interface</a>
