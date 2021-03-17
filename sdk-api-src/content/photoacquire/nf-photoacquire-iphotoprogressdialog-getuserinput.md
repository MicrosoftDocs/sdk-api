---
UID: NF:photoacquire.IPhotoProgressDialog.GetUserInput
title: IPhotoProgressDialog::GetUserInput (photoacquire.h)
description: Retrieves descriptive information entered by the user, such as the tag name of the images to store.
helpviewer_keywords: ["GetUserInput","GetUserInput method [Picture Acquisition]","GetUserInput method [Picture Acquisition]","IPhotoProgressDialog interface","IPhotoProgressDialog interface [Picture Acquisition]","GetUserInput method","IPhotoProgressDialog.GetUserInput","IPhotoProgressDialog::GetUserInput","IPhotoProgressDialogGetUserInput","photoacquire/IPhotoProgressDialog::GetUserInput","picacq.iphotoprogressdialog_getuserinput"]
old-location: picacq\iphotoprogressdialog_getuserinput.htm
tech.root: picacq
ms.assetid: 1f797e68-f87d-4f90-853b-60c6c9309f58
ms.date: 12/05/2018
ms.keywords: GetUserInput, GetUserInput method [Picture Acquisition], GetUserInput method [Picture Acquisition],IPhotoProgressDialog interface, IPhotoProgressDialog interface [Picture Acquisition],GetUserInput method, IPhotoProgressDialog.GetUserInput, IPhotoProgressDialog::GetUserInput, IPhotoProgressDialogGetUserInput, photoacquire/IPhotoProgressDialog::GetUserInput, picacq.iphotoprogressdialog_getuserinput
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
 - IPhotoProgressDialog::GetUserInput
 - photoacquire/IPhotoProgressDialog::GetUserInput
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
 - IPhotoProgressDialog.GetUserInput
---

# IPhotoProgressDialog::GetUserInput


## -description

Retrieves descriptive information entered by the user, such as the tag name of the images to store.

## -parameters

### -param riidType [in]

Specifies the interface identifier (ID) of the prompt type. Currently, the only supported value is IID_IUserInputString.

### -param pUnknown [in]

Pointer to an object of the prompt class. Currently, the only supported type is <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString</a>.

### -param pPropVarResult [out]

Pointer to a property variant that stores the user input. Must be freed by the caller using <b>ClearPropVariant</b>.

### -param pPropVarDefault [in]

Pointer to a property variant containing the default value to be used if no input is supplied.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The progress dialog has been suppressed

</td>
</tr>
</table>

## -remarks

If the progress dialog box has been suppressed in <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a>, and <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireprogresscb-getuserinput">IPhotoAcquireProgressCB::GetUserInput</a> is either not implemented, or returns E_NOTIMPL, this method will return S_FALSE, and <i>pPropVarResult</i> will contain the value stored in the optional <i>pPropVarDefault</i> argument.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoprogressdialog">IPhotoProgressDialog Interface</a>