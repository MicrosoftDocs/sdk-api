---
UID: NF:photoacquire.IPhotoAcquireProgressCB.ErrorAdvise
title: IPhotoAcquireProgressCB::ErrorAdvise
author: windows-driver-content
description: The ErrorAdvise method provides custom error handling for errors that occur during acquisition. The application provides the implementation of the ErrorAdvise method.
old-location: picacq\iphotoacquireprogresscb_erroradvise.htm
old-project: acquisition
ms.assetid: 60454ae7-9be9-4414-9865-2b874bbe54c1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ErrorAdvise, ErrorAdvise method [Picture Acquisition], ErrorAdvise method [Picture Acquisition],IPhotoAcquireProgressCB interface, IPhotoAcquireProgressCB interface [Picture Acquisition],ErrorAdvise method, IPhotoAcquireProgressCB.ErrorAdvise, IPhotoAcquireProgressCB::ErrorAdvise, IPhotoAcquireProgressCBErrorAdvise, photoacquire/IPhotoAcquireProgressCB::ErrorAdvise, picacq.iphotoacquireprogresscb_erroradvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoAcquireProgressCB.ErrorAdvise
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<th>
                  Value
                </th>
<th>
                  Description
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
<th>
                  Value
                </th>
<th>
                  Description
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




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

