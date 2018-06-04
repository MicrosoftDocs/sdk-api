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

# SetupQueueRenameW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueRename</b> function places an individual file rename operation on a setup file queue.


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


### -param SourcePath [in]

Pointer to a null-terminated string that specifies the source path of the file to be renamed. If <i>SourceFileName</i> is not specified, <i>SourcePath</i> is assumed to be the full path.


### -param SourceFilename

TBD


### -param TargetPath [in]

Pointer to a null-terminated string that specifies the target directory. When this parameter is specified, the rename operation is actually a move operation. If <i>TargetPath</i> is not specified, the file is renamed but remains in its current location.


### -param TargetFilename

TBD




#### - SourceFileName [in]

Pointer to a null-terminated string that specifies the file name part of the file to be renamed. If not specified, <i>SourcePath</i> is the full path.


#### - TargetFileName [in]

Pointer to a null-terminated string that specifies the new name for the source file.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because rename operations are assumed to take place on fixed media, the user will not be prompted when the queue is committed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a>



<a href="https://msdn.microsoft.com/21cdaf05-c4fb-4130-baa5-31baf5391ece">SetupQueueDelete</a>



<a href="https://msdn.microsoft.com/8ac93cfa-cfe4-4747-813d-512963d0d87c">SetupQueueRenameSection</a>
 

 

