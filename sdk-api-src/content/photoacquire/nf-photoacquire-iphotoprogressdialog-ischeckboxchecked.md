---
UID: NF:photoacquire.IPhotoProgressDialog.IsCheckboxChecked
title: IPhotoProgressDialog::IsCheckboxChecked (photoacquire.h)
description: The IsCheckboxChecked method indicates whether the check box in the progress dialog box (typically indicating whether to delete files after transfer) is selected.
old-location: picacq\iphotoprogressdialog_ischeckboxchecked.htm
tech.root: acquisition
ms.assetid: 05810577-c23a-4f75-9cd5-0b5b6be7d181
ms.date: 12/05/2018
ms.keywords: IPhotoProgressDialog interface [Picture Acquisition],IsCheckboxChecked method, IPhotoProgressDialog.IsCheckboxChecked, IPhotoProgressDialog::IsCheckboxChecked, IPhotoProgressDialogIsCheckboxChecked, IsCheckboxChecked, IsCheckboxChecked method [Picture Acquisition], IsCheckboxChecked method [Picture Acquisition],IPhotoProgressDialog interface, photoacquire/IPhotoProgressDialog::IsCheckboxChecked, picacq.iphotoprogressdialog_ischeckboxchecked
ms.topic: method
f1_keywords:
- photoacquire/IPhotoProgressDialog.IsCheckboxChecked
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- PhotoAcquireUID.lib
- PhotoAcquireUID.dll
api_name:
- IPhotoProgressDialog.IsCheckboxChecked
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoProgressDialog::IsCheckboxChecked


## -description



The <code>IsCheckboxChecked</code> method indicates whether the check box in the progress dialog box (typically indicating whether to delete files after transfer) is selected.




## -parameters




### -param nCheckboxId [in]

Integer value containing the check box identifier (ID).


### -param pfChecked [out]

Pointer to a flag that, if set to <b>TRUE</b>, indicates that the check box is selected.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>
 

 

