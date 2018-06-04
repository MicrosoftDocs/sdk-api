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

# CoRegisterSurrogate function


## -description


Registers the surrogate process through its <a href="https://msdn.microsoft.com/fbed0514-3646-4744-aa7a-4a98f1a12cc0">ISurrogate</a> interface pointer.


## -parameters




### -param pSurrogate [in]

A pointer to the <a href="https://msdn.microsoft.com/fbed0514-3646-4744-aa7a-4a98f1a12cc0">ISurrogate</a> interface on the surrogate process to be registered.


## -returns



This function returns S_OK to indicate that the surrogate process was registered successfully.




## -remarks



The <b>CoRegisterSurrogate</b> function sets a global interface pointer to the <a href="https://msdn.microsoft.com/fbed0514-3646-4744-aa7a-4a98f1a12cc0">ISurrogate</a> interface implemented on the surrogate process. This pointer is set in the ole32 DLL loaded in the surrogate process. COM uses this global pointer in ole32 to call the methods of <b>ISurrogate</b>. This function is usually called by the surrogate implementation when it is launched.



As of Windows Server 2003, if a COM object application is registered as a service, COM verifies the registration. COM makes sure the process ID of the service, in the service control manager (SCM), matches the process ID of the registering process. If not, COM fails the registration.




## -see-also




<a href="https://msdn.microsoft.com/fbed0514-3646-4744-aa7a-4a98f1a12cc0">ISurrogate</a>



<a href="https://msdn.microsoft.com/510e38e5-1965-46f4-b09c-6fa585cff993">Writing a Custom Surrogate</a>
 

 

