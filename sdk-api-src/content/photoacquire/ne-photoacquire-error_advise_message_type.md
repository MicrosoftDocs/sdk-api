---
UID: NE:photoacquire.tagERROR_ADVISE_MESSAGE_TYPE
title: ERROR_ADVISE_MESSAGE_TYPE
author: windows-sdk-content
description: The ERROR_ADVISE_MESSAGE_TYPE enumeration type indicates the type of error values that can be passed to the nMessageType parameter of IPhotoAcquireProgressCB::ErrorAdvise.
old-location: picacq\error_advise_message_type.htm
tech.root: acquisition
ms.assetid: 2fde8aa9-126a-4908-8faf-71ecad231f8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ERROR_ADVISE_MESSAGE_TYPE, ERROR_ADVISE_MESSAGE_TYPE enumeration [Picture Acquisition], PHOTOACQUIRE_ERROR_OK, PHOTOACQUIRE_ERROR_RETRYCANCEL, PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL, PHOTOACQUIRE_ERROR_YESNO, enumeration [Picture Acquisition], photoacquire/ERROR_ADVISE_MESSAGE_TYPE, photoacquire/PHOTOACQUIRE_ERROR_OK, photoacquire/PHOTOACQUIRE_ERROR_RETRYCANCEL, photoacquire/PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL, photoacquire/PHOTOACQUIRE_ERROR_YESNO, picacq.error_advise_message_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PhotoAcquire.h
api_name:
 - ERROR_ADVISE_MESSAGE_TYPE
product: Windows
targetos: Windows
req.typenames: ERROR_ADVISE_MESSAGE_TYPE
req.redist: 
---

# ERROR_ADVISE_MESSAGE_TYPE enumeration


## -description



The <code>ERROR_ADVISE_MESSAGE_TYPE</code> enumeration type indicates the type of error values that can be passed to the <i>nMessageType</i> parameter of <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>.




## -enum-fields




### -field PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL

Specifies that the error that occurred requires a Skip, Retry, or Cancel response. The <i>pnErrorAdviseResult</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressDialogCB::ErrorAdvise</a> must be one of the following: <b>PHOTOACQUIRE_RESULT_SKIP</b>, <b>PHOTOACQUIRE_RESULT_SKIP_ALL</b>, <b>PHOTOACQUIRE_RESULT_RETRY</b>, or <b>PHOTOACQUIRE_RESULT_ABORT</b>.


### -field PHOTOACQUIRE_ERROR_RETRYCANCEL

Specifies that the error that occurred requires a Retry or Cancel response. The <i>pnErrorAdviseResult</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressDialogCB::ErrorAdvise</a> must be one of the following: <b>PHOTOACQUIRE_RESULT_RETRY</b> or <b>PHOTOACQUIRE_RESULT_ABORT</b>.


### -field PHOTOACQUIRE_ERROR_YESNO

Specifies that the error that occurred requires a Yes or No response. The <i>pnErrorAdviseResult</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressDialogCB::ErrorAdvise</a> must be one of the following: <b>PHOTOACQUIRE_RESULT_YES</b> or <b>PHOTOACQUIRE_RESULT_NO</b>.


### -field PHOTOACQUIRE_ERROR_OK

Specifies that the error that occurred requires an OK response. The <i>pnErrorAdviseResult</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressDialogCB::ErrorAdvise</a> must be <b>PHOTOACQUIRE_RESULT_OK</b>.


## -see-also




<a href="https://msdn.microsoft.com/a3cb2a2d-049a-4607-beaf-41ea6f0d4704">ERROR_ADVISE_RESULT</a>



<a href="https://msdn.microsoft.com/767d20df-aeb4-4f86-a705-bfbb7dc254ff">Enumeration Types</a>



<a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>
 

 

