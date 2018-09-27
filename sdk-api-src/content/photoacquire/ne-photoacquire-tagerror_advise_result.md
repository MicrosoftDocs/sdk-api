---
UID: NE:photoacquire.tagERROR_ADVISE_RESULT
title: tagERROR_ADVISE_RESULT
author: windows-sdk-content
description: The ERROR_ADVISE_RESULT enumeration type indicates the type of error values that can be assigned to the pnErrorAdviseResult parameter of IPhotoAcquireProgressCB::ErrorAdvise.
old-location: picacq\error_advise_result.htm
tech.root: acquisition
ms.assetid: a3cb2a2d-049a-4607-beaf-41ea6f0d4704
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ERROR_ADVISE_RESULT, ERROR_ADVISE_RESULT enumeration [Picture Acquisition], PHOTOACQUIRE_RESULT_ABORT, PHOTOACQUIRE_RESULT_NO, PHOTOACQUIRE_RESULT_OK, PHOTOACQUIRE_RESULT_RETRY, PHOTOACQUIRE_RESULT_SKIP, PHOTOACQUIRE_RESULT_SKIP_ALL, PHOTOACQUIRE_RESULT_YES, enumeration [Picture Acquisition], photoacquire/ERROR_ADVISE_RESULT, photoacquire/PHOTOACQUIRE_RESULT_ABORT, photoacquire/PHOTOACQUIRE_RESULT_NO, photoacquire/PHOTOACQUIRE_RESULT_OK, photoacquire/PHOTOACQUIRE_RESULT_RETRY, photoacquire/PHOTOACQUIRE_RESULT_SKIP, photoacquire/PHOTOACQUIRE_RESULT_SKIP_ALL, photoacquire/PHOTOACQUIRE_RESULT_YES, picacq.error_advise_result, tagERROR_ADVISE_RESULT
ms.prod: windows
ms.technology: windows-sdk
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
 - ERROR_ADVISE_RESULT
product: Windows
targetos: Windows
req.typenames: ERROR_ADVISE_RESULT
req.redist: 
---

# tagERROR_ADVISE_RESULT enumeration


## -description



The <code>ERROR_ADVISE_RESULT</code> enumeration type indicates the type of error values that can be assigned to the <i>pnErrorAdviseResult</i> parameter of <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>.




## -enum-fields




### -field PHOTOACQUIRE_RESULT_YES

Specifies a Yes response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_YESNO.


### -field PHOTOACQUIRE_RESULT_NO

Specifies a No response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_YESNO.


### -field PHOTOACQUIRE_RESULT_OK

Specifies an OK response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_OK.


### -field PHOTOACQUIRE_RESULT_SKIP

Specifies a Skip response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL.


### -field PHOTOACQUIRE_RESULT_SKIP_ALL

Specifies a Skip All response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL.


### -field PHOTOACQUIRE_RESULT_RETRY

Specifies a Retry response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL or PHOTOACQUIRE_ERROR_RETRYCANCEL.


### -field PHOTOACQUIRE_RESULT_ABORT

Specifies a Cancel response to an error dialog. Valid only if the <i>nMessageType</i> parameter to <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a> is PHOTOACQUIRE_ERROR_SKIPRETRYCANCEL or PHOTOACQUIRE_ERROR_RETRYCANCEL.


## -remarks



The type of response allowed is of type <a href="https://msdn.microsoft.com/2fde8aa9-126a-4908-8faf-71ecad231f8d">ERROR_ADVISE_MESSAGE_TYPE</a>, and indicated by the <i>nMessageType</i> parameter of <a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>.




## -see-also




<a href="https://msdn.microsoft.com/2fde8aa9-126a-4908-8faf-71ecad231f8d">ERROR_ADVISE_MESSAGE_TYPE</a>



<a href="https://msdn.microsoft.com/767d20df-aeb4-4f86-a705-bfbb7dc254ff">Enumeration Types</a>



<a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>
 

 

