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

# RenameTransactionManager function


## -description


Renames a transaction manager (TM) object. This function can only be used on named TM 
    handles. A new <b>GUID</b> for the TM is selected and can be retrieved using the 
    <a href="https://msdn.microsoft.com/e1aa573d-add9-42b7-8b2b-773dc12aa51b">GetTransactionManagerID</a> function.


## -parameters




### -param LogFileName [in]

The name of the log stream.  This stream must exist within a CLFS log file.


### -param ExistingTransactionManagerGuid [in]

A value that specifies the current name of the TM.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/e1aa573d-add9-42b7-8b2b-773dc12aa51b">GetTransactionManagerID</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

