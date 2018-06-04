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

# FhServiceUnblockBackup function


## -description


This function unblocks backups blocked via <a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a>.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function removes the effects of a prior <a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a> call issued via a given communication channel with the File History Service.




## -see-also




<a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a>



<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>
 

 

