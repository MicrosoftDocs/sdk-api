---
UID: NF:photoacquire.IPhotoAcquireProgressCB.GetUserInput
title: IPhotoAcquireProgressCB::GetUserInput (photoacquire.h)
description: The GetUserInput method overrides the default functionality that displays a message prompting the user for string input during acquisition. The application provides the implementation of the GetUserInput method.
helpviewer_keywords: ["GetUserInput","GetUserInput method [Picture Acquisition]","GetUserInput method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","GetUserInput method","IPhotoAcquireProgressCB.GetUserInput","IPhotoAcquireProgressCB::GetUserInput","IPhotoAcquireProgressCBGetUserInput","photoacquire/IPhotoAcquireProgressCB::GetUserInput","picacq.iphotoacquireprogresscb_getuserinput"]
old-location: picacq\iphotoacquireprogresscb_getuserinput.htm
tech.root: picacq
ms.assetid: db0d924b-a586-4f81-a367-e8fbdf3e9bd9
ms.date: 12/05/2018
ms.keywords: GetUserInput, GetUserInput method [Picture Acquisition], GetUserInput method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],GetUserInput method, IPhotoAcquireProgressCB.GetUserInput, IPhotoAcquireProgressCB::GetUserInput, IPhotoAcquireProgressCBGetUserInput, photoacquire/IPhotoAcquireProgressCB::GetUserInput, picacq.iphotoacquireprogresscb_getuserinput
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
 - IPhotoAcquireProgressCB::GetUserInput
 - photoacquire/IPhotoAcquireProgressCB::GetUserInput
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
 - IPhotoAcquireProgressCB.GetUserInput
---

# IPhotoAcquireProgressCB::GetUserInput


## -description

The <code>GetUserInput</code> method overrides the default functionality that displays a message prompting the user for string input during acquisition. The application provides the implementation of the <code>GetUserInput</code> method.

## -parameters

### -param riidType [in]

Specifies the interface ID of the prompt type. This may only be IID_IUserInputString.

### -param pUnknown [in]

Pointer to an object of the prompt class. Currently, this must be an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString</a> object.

### -param pPropVarResult [out]

Pointer to a property variant object representing the descriptive input to be obtained. Must be freed by the caller using PropVariantClear.

If the application's implementation of <code>GetUserInput</code> returns a value other than E_NOTIMPL, the value of <i>pPropVarDefault</i> must be copied to the <i>pPropVarResult</i> parameter.

### -param pPropVarDefault [in]

Pointer to a property variant object representing the default value of the input being requested.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Return E_NOTIMPL if the default functionality is desired

</td>
</tr>
</table>

## -remarks

If this method is implemented, the implementation should copy the value of the <i>pPropVarDefault</i> argument to the <i>pPropVarResult</i> parameter.

If this method returns an HRESULT other than E_NOTIMPL, the default dialog box that prompts the user will not be displayed.

If the progress dialog box is suppressed in <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a>, this method must be implemented in order to assign a default value to the <i>pPropVarResult</i> parameter. Normally a value is supplied to <i>pPropVarResult</i> in the course of prompting the user with the default dialog, but when the dialog is suppressed, the application must copy the value of the <i>pPropVarDefault</i> argument to the <i>pPropVarResult</i> parameter.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>