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

# RegisterOnlineBackupWithWindowsServerBackup function


## -description


The <b>RegisterOnlineBackupWithWindowsServerBackup</b> function registers a cloud backup provider with Windows Server Backup.


## -parameters




### -param pOBRegistrationInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/E01EF90E-90F1-4B56-85B8-63A10A688FBA">WSB_OB_REGISTRATION_INFO</a> structure.


## -returns



The return values listed here are in addition to the normal <b>HRESULT</b>s that may be returned at any time 
       from the function.




## -remarks



If any other cloud backup provider is already registered with Windows Server Backup, <a href="https://msdn.microsoft.com/4E70EF3D-E4AA-498C-B131-8C5F48CD230E">DeregisterOnlineBackupFromWindowsServerBackup</a> must be called before calling <b>RegisterOnlineBackupWithWindowsServerBackup</b>.




## -see-also




<a href="https://msdn.microsoft.com/61F77E92-19EF-4409-9435-CD03ACCE810D">Cloud  Backup Provider API Functions</a>



<a href="https://msdn.microsoft.com/E01EF90E-90F1-4B56-85B8-63A10A688FBA">WSB_OB_REGISTRATION_INFO</a>
 

 

