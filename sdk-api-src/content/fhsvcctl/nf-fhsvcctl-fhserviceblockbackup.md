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

# FhServiceBlockBackup function


## -description


This function temporarily blocks backups for the current user.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function instructs the File History Service to not perform backups for the current user until the <a href="https://msdn.microsoft.com/4CCCEEA5-40BC-4862-ADF5-C8757E02916A">FhServiceUnblockBackup</a> function is called or the communication channel with the File History Service is closed by calling <a href="https://msdn.microsoft.com/20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7">FhServiceClosePipe</a>.

Call this function prior to performing File History configuration reassociation to ensure that File History configuration and data files are not currently in use. (Otherwise, the <a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a> method may fail.)




## -see-also




<a href="https://msdn.microsoft.com/20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7">FhServiceClosePipe</a>



<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>



<a href="https://msdn.microsoft.com/4CCCEEA5-40BC-4862-ADF5-C8757E02916A">FhServiceUnblockBackup</a>



<a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a>
 

 

