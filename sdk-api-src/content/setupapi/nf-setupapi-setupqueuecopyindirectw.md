---
UID: NF:setupapi.SetupQueueCopyIndirectW
title: SetupQueueCopyIndirectW function
author: windows-driver-content
description: The SetupQueueCopyIndirect function is an extended form of SetupQueueCopy passing additional parameters as a structure (SP_FILE_COPY_PARAMS). Other than this, the behavior is identical.
old-location: setup\setupqueuecopyindirect.htm
old-project: SetupApi
ms.assetid: 5c81e83c-7ee3-489f-9d4c-f7c8a1c5cc5b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetupQueueCopyIndirect, SetupQueueCopyIndirect function [Setup API], SetupQueueCopyIndirectA, SetupQueueCopyIndirectW, _setupapi_setupqueuecopyindirect, setup.setupqueuecopyindirect, setupapi/SetupQueueCopyIndirect, setupapi/SetupQueueCopyIndirectA, setupapi/SetupQueueCopyIndirectW
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
req.unicode-ansi: SetupQueueCopyIndirectW (Unicode) and SetupQueueCopyIndirectA (ANSI)
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
-	SetupQueueCopyIndirect
-	SetupQueueCopyIndirectA
-	SetupQueueCopyIndirectW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SetupQueueCopyIndirectW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueCopyIndirect</b> function is an extended form of 
<a href="https://msdn.microsoft.com/c8683438-7a28-4713-8781-45f9bd75b72c">SetupQueueCopy</a> passing additional parameters as a structure (<a href="https://msdn.microsoft.com/4c4d418d-e279-40ea-9ec1-42ced523db34">SP_FILE_COPY_PARAMS</a>). Other than this, the behavior is identical.


## -parameters




### -param CopyParams [in]

Pointer to a 
<a href="https://msdn.microsoft.com/4c4d418d-e279-40ea-9ec1-42ced523db34">SP_FILE_COPY_PARAMS</a> structure that describes the file copy operation.


## -returns



If the function succeeds, the return value is an nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists before the queue is committed. The setup functions do not check for the existence of and do not create UNC directories. If the target UNC directory does not exist, the file copy will fail.



