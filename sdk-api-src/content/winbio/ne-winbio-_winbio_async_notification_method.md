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

# _WINBIO_ASYNC_NOTIFICATION_METHOD enumeration


## -description


Defines constants that specify how completion notifications for asynchronous operations are to be delivered to the client application. This enumeration is used by the <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a> and <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> functions.


## -enum-fields




### -field WINBIO_ASYNC_NOTIFY_NONE

The operation is synchronous.


### -field WINBIO_ASYNC_NOTIFY_CALLBACK

The client-implemented <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function is called by the framework.


### -field WINBIO_ASYNC_NOTIFY_MESSAGE

The framework sends completion notices to the client application window message queue.


### -field WINBIO_ASYNC_NOTIFY_MAXIMUM_VALUE

The maximum enumeration value. This constant is not directly used by the <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a> and <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>.


## -remarks



This enumeration was introduced in Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/fd33bc63-cc99-40de-a43b-b0bc7d4c9454">Client Application Enumerations</a>



<a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>



<a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>
 

 

