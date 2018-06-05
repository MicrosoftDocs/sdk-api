---
UID: NF:setupapi.SetupQueueDeleteA
title: SetupQueueDeleteA function
author: windows-sdk-content
description: The SetupQueueDelete function places an individual file delete operation on a setup file queue.
old-location: setup\setupqueuedelete.htm
old-project: SetupApi
ms.assetid: 21cdaf05-c4fb-4130-baa5-31baf5391ece
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupQueueDelete, SetupQueueDelete function [Setup API], SetupQueueDeleteA, SetupQueueDeleteW, _setupapi_setupqueuedelete, setup.setupqueuedelete, setupapi/SetupQueueDelete, setupapi/SetupQueueDeleteA, setupapi/SetupQueueDeleteW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueueDeleteW (Unicode) and SetupQueueDeleteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupQueueDelete
-	SetupQueueDeleteA
-	SetupQueueDeleteW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupQueueDeleteA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDelete</b> function places an individual file delete operation on a setup file queue.


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


### -param PathPart1 [in]

Pointer to a <b>null</b>-terminated string that specifies the first part of the path of the file to be deleted. If <i>PathPart2</i> is <b>NULL</b>, <i>PathPart1</i> is the full path of the file to be deleted.


### -param PathPart2 [in]

Pointer to a <b>null</b>-terminated string that specifies the second part of the path of the file to be deleted. This parameter may be <b>NULL</b>. This is appended to <i>PathPart1</i> to form the full path of the file to be deleted. The function checks for and collapses duplicated path separators when it combines <i>PathPart1</i> and <i>PathPart2</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because delete operations are assumed to take place on fixed media, the user will not be prompted when the queue is committed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a>



<a href="https://msdn.microsoft.com/3e76e345-1d6c-4eb5-a743-b71d5ccc52e5">SetupQueueDeleteSection</a>



<a href="https://msdn.microsoft.com/0b80eba9-9e71-4255-8c1b-039878682ec4">SetupQueueRename</a>
 

 

