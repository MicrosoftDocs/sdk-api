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

# GetEnlistmentRecoveryInformation function


## -description


 Retrieves an opaque structure of recovery data from KTM.  Recovery information is stored in a log on behalf of a resource manager (RM) by calling the <a href="https://msdn.microsoft.com/54e7526f-57f0-40cd-9624-fce0644a0884">SetEnlistmentRecoveryInformation</a> function.  After a failure, the RM can use the <b>GetEnlistmentRecoveryInformation</b> function to retrieve the information.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param BufferSize [in]

The size of the <i>Buffer</i> parameter, in bytes.


### -param Buffer [out]

A pointer to a buffer that receives the enlistment recovery information.


### -param OPTIONAL

TBD




#### - BufferUsed [out, optional]

A pointer to a variable that receives the actual number of bytes returned in the <i>Buffer</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



This call cannot be used with volatile transaction managers.




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/54e7526f-57f0-40cd-9624-fce0644a0884">SetEnlistmentRecoveryInformation</a>
 

 

