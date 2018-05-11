---
UID: NF:setupapi.SetupOpenFileQueue
title: SetupOpenFileQueue function
author: windows-driver-content
description: The SetupOpenFileQueue function creates a setup file queue.
old-location: setup\setupopenfilequeue.htm
old-project: SetupApi
ms.assetid: 36950f18-80ae-46b7-9f9f-bd5307d72a3b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupOpenFileQueue, SetupOpenFileQueue function [Setup API], _setupapi_setupopenfilequeue, setup.setupopenfilequeue, setupapi/SetupOpenFileQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: 
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupOpenFileQueue
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupOpenFileQueue function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenFileQueue</b> function creates a setup file queue.


## -parameters






## -returns



If the function succeeds, it returns a handle to a setup file queue. If there is not enough memory to create the queue, the function returns INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the file queue has been committed and is no longer needed, 
<a href="https://msdn.microsoft.com/51c63e65-a844-46b4-93ef-8a92a9c8a604">SetupCloseFileQueue</a> should be called to release the resources allocated during 
<b>SetupOpenFileQueue</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/51c63e65-a844-46b4-93ef-8a92a9c8a604">SetupCloseFileQueue</a>



<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>



<a href="https://msdn.microsoft.com/04db1553-1c9a-414e-a2b8-b087dd44ef55">SetupInstallFile</a>



<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a>



<a href="https://msdn.microsoft.com/21cdaf05-c4fb-4130-baa5-31baf5391ece">SetupQueueDelete</a>



<a href="https://msdn.microsoft.com/0b80eba9-9e71-4255-8c1b-039878682ec4">SetupQueueRename</a>
 

 

