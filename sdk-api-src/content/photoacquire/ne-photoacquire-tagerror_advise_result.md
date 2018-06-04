---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>
 

 

