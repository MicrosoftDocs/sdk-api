---
UID: NF:photoacquire.IPhotoAcquireProgressCB.ErrorAdvise
title: IPhotoAcquireProgressCB::ErrorAdvise (photoacquire.h)
description: The ErrorAdvise method provides custom error handling for errors that occur during acquisition. The application provides the implementation of the ErrorAdvise method.
helpviewer_keywords: ["ErrorAdvise","ErrorAdvise method [Picture Acquisition]","ErrorAdvise method [Picture Acquisition]","IPhotoAcquireProgressCB interface","IPhotoAcquireProgressCB interface [Picture Acquisition]","ErrorAdvise method","IPhotoAcquireProgressCB.ErrorAdvise","IPhotoAcquireProgressCB::ErrorAdvise","IPhotoAcquireProgressCBErrorAdvise","photoacquire/IPhotoAcquireProgressCB::ErrorAdvise","picacq.iphotoacquireprogresscb_erroradvise"]
old-location: picacq\iphotoacquireprogresscb_erroradvise.htm
tech.root: picacq
ms.assetid: 60454ae7-9be9-4414-9865-2b874bbe54c1
ms.date: 12/05/2018
ms.keywords: ErrorAdvise, ErrorAdvise method [Picture Acquisition], ErrorAdvise method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],ErrorAdvise method, IPhotoAcquireProgressCB.ErrorAdvise, IPhotoAcquireProgressCB::ErrorAdvise, IPhotoAcquireProgressCBErrorAdvise, photoacquire/IPhotoAcquireProgressCB::ErrorAdvise, picacq.iphotoacquireprogresscb_erroradvise
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
 - IPhotoAcquireProgressCB::ErrorAdvise
 - photoacquire/IPhotoAcquireProgressCB::ErrorAdvise
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
 - IPhotoAcquireProgressCB.ErrorAdvise
---

# IPhotoAcquireProgressCB::ErrorAdvise


## -description

The <code>ErrorAdvise</code> method provides custom error handling for errors that occur during acquisition. The application provides the implementation of the <code>ErrorAdvise</code> method.

## -parameters

### -param hr [in]

Specifies the error that occurred.

### -param pszErrorMessage [in]

Pointer to a null-terminated string containing the error message.

### -param nMessageType [in]

Integer value containing the message type. May be one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL
                </b></td>
<td>Specifies that the error that occurred requires a Skip, Retry, or Cancel response. The <i>pnErrorAdviseResult</i> parameter must be set to one of the following: <b>PHOTOACQUIRE_RESULT_SKIP</b>, <b>PHOTOACQUIRE_RESULT_SKIP_ALL</b>, <b>PHOTOACQUIRE_RESULT_RETRY</b>, or <b>PHOTOACQUIRE_RESULT_ABORT</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_ERROR_RETRYCANCEL</b></td>
<td>Specifies that the error that occurred requires a Retry or Cancel response. The <i>pnErrorAdviseResult</i> parameter must be set to one of the following: <b>PHOTOACQUIRE_RESULT_RETRY</b> or <b>PHOTOACQUIRE_RESULT_ABORT</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_ERROR_YESNO</b></td>
<td>Specifies that the error that occurred requires a Yes or No response. The <i>pnErrorAdviseResult</i> parameter must be set to one of the following: <b>PHOTOACQUIRE_RESULT_YES</b> or <b>PHOTOACQUIRE_RESULT_NO</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_ERROR_OK</b></td>
<td>Specifies that the error that occurred requires an OK response. The <i>pnErrorAdviseResult</i> parameter must be set to <b>PHOTOACQUIRE_RESULT_OK</b>.</td>
</tr>
</table>

### -param pnErrorAdviseResult [out]

Pointer to an integer value containing the error advise result. The result should be one of the acceptable types indicated by the <i>nMessageType</i> parameter, and must be one of the following:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_YES</b></td>
<td>Specifies a Yes response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_YESNO</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_NO</b></td>
<td>Specifies a No response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_YESNO</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_OK</b></td>
<td>Specifies an OK response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_OK</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_SKIP</b></td>
<td>Specifies a Skip response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_SKIP_ALL</b></td>
<td>Specifies a Skip All response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_RETRY</b></td>
<td>Specifies a Retry response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL</b> or <b>PHOTOACQUIRE_ERROR_RETRYCANCEL</b>.</td>
</tr>
<tr>
<td><b>PHOTOACQUIRE_RESULT_ABORT</b></td>
<td>Specifies a Cancel response. Valid if <i>nMessageType</i> is <b>PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL</b> or <b>PHOTOACQUIRE_ERROR_RETRYCANCEL</b>.</td>
</tr>
</table>

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
The method is not yet implemented

</td>
</tr>
</table>

## -remarks

Normally, a message is displayed when an error occurs during image acquisition. If suppression of this message is desired, implement <code>ErrorAdvise</code>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>