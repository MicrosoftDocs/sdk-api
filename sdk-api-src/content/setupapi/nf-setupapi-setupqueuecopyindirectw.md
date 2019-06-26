---
UID: NF:setupapi.SetupQueueCopyIndirectW
title: SetupQueueCopyIndirectW function (setupapi.h)
author: windows-sdk-content
description: The SetupQueueCopyIndirect function is an extended form of SetupQueueCopy passing additional parameters as a structure (SP_FILE_COPY_PARAMS). Other than this, the behavior is identical.
old-location: setup\setupqueuecopyindirect.htm
tech.root: SetupApi
ms.assetid: 5c81e83c-7ee3-489f-9d4c-f7c8a1c5cc5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupQueueCopyIndirect, SetupQueueCopyIndirect function [Setup API], SetupQueueCopyIndirectA, SetupQueueCopyIndirectW, _setupapi_setupqueuecopyindirect, setup.setupqueuecopyindirect, setupapi/SetupQueueCopyIndirect, setupapi/SetupQueueCopyIndirectA, setupapi/SetupQueueCopyIndirectW
ms.topic: function
f1_keywords: 
 - "setupapi/SetupQueueCopyIndirect"
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQueueCopyIndirect
 - SetupQueueCopyIndirectA
 - SetupQueueCopyIndirectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupQueueCopyIndirectW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueCopyIndirect</b> function is an extended form of 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupqueuecopya">SetupQueueCopy</a> passing additional parameters as a structure (<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-_sp_file_copy_params_a">SP_FILE_COPY_PARAMS</a>). Other than this, the behavior is identical.


## -parameters




### -param CopyParams [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-_sp_file_copy_params_a">SP_FILE_COPY_PARAMS</a> structure that describes the file copy operation.


## -returns



If the function succeeds, the return value is an nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If a UNC directory is specified as the target directory of a file copy operation, you must ensure it exists before the queue is committed. The setup functions do not check for the existence of and do not create UNC directories. If the target UNC directory does not exist, the file copy will fail.



