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

# INTERNET_AUTH_NOTIFY_DATA structure


## -description


Contains the notification data for an authentication request.


## -struct-fields




### -field cbStruct

Size of the structure, in bytes. 


### -field dwOptions


### -field pfnNotify

Notification callback to retry 
<a href="https://msdn.microsoft.com/09384ba9-e5cc-48fd-a52c-15df223f87dc">InternetErrorDlg</a>. 


### -field dwContext

Pointer to a variable that contains an application-defined value used to identify the application context to pass to the notification function. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/09384ba9-e5cc-48fd-a52c-15df223f87dc">InternetErrorDlg</a>
 

 

