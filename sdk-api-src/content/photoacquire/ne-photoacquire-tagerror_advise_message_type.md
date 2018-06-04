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

# tagERROR_ADVISE_MESSAGE_TYPE enumeration


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



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/60454ae7-9be9-4414-9865-2b874bbe54c1">IPhotoAcquireProgressCB::ErrorAdvise</a>
 

 

