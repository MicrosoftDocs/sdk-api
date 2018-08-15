---
UID: NF:setupapi.SetupCloseFileQueue
title: SetupCloseFileQueue function
author: windows-sdk-content
description: The SetupCloseFileQueue function destroys a setup file queue.
old-location: setup\setupclosefilequeue.htm
old-project: SetupApi
ms.assetid: 51c63e65-a844-46b4-93ef-8a92a9c8a604
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetupCloseFileQueue, SetupCloseFileQueue function [Setup API], _setupapi_setupclosefilequeue, setup.setupclosefilequeue, setupapi/SetupCloseFileQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupCloseFileQueue
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupCloseFileQueue function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCloseFileQueue</b> function destroys a setup file queue.


## -parameters




### -param QueueHandle [in]

Handle to an open setup file queue.


## -returns



This function does not return a value.




## -remarks



The 
<b>SetupCloseFileQueue</b> function does not flush the queue; pending operations are not performed. To commit a file queue before closing it call 
<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>



<a href="https://msdn.microsoft.com/04db1553-1c9a-414e-a2b8-b087dd44ef55">SetupInstallFile</a>



<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a>



<a href="https://msdn.microsoft.com/57e8dc72-5b0e-486c-9819-fa44085580eb">SetupQueueDefaultCopy</a>



<a href="https://msdn.microsoft.com/21cdaf05-c4fb-4130-baa5-31baf5391ece">SetupQueueDelete</a>



<a href="https://msdn.microsoft.com/0b80eba9-9e71-4255-8c1b-039878682ec4">SetupQueueRename</a>
 

 

