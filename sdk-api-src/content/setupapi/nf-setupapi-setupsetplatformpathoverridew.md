---
UID: NF:setupapi.SetupSetPlatformPathOverrideW
title: SetupSetPlatformPathOverrideW function
author: windows-sdk-content
description: The SetupSetPlatformPathOverride function is used to set a platform path override for a target machine when working with INFs from a different machine.
old-location: setup\setupsetplatformpathoverride.htm
old-project: SetupApi
ms.assetid: 98867613-18d8-4954-b37a-39c442756bbc
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SetupSetPlatformPathOverride, SetupSetPlatformPathOverride function [Setup API], SetupSetPlatformPathOverrideA, SetupSetPlatformPathOverrideW, _setupapi_setupsetplatformpathoverride, setup.setupsetplatformpathoverride, setupapi/SetupSetPlatformPathOverride, setupapi/SetupSetPlatformPathOverrideA, setupapi/SetupSetPlatformPathOverrideW
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
req.unicode-ansi: SetupSetPlatformPathOverrideW (Unicode) and SetupSetPlatformPathOverrideA (ANSI)
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
 - SetupSetPlatformPathOverride
 - SetupSetPlatformPathOverrideA
 - SetupSetPlatformPathOverrideW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupSetPlatformPathOverrideW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetPlatformPathOverride</b> function is used to set a platform path override for a  target machine when working with INFs from a different machine. As such, it can refer to a different platform than it is currently running on. For dealing with media sources, it can refer to  platforms that are no longer supported, such as Alpha, MIPS, and PPC. It removes the platform path override if none is specified. 


## -parameters




### -param Override [in]

Pointer to a <b>null</b>-terminated string that contains the replacement platform information. For example, "alpha" or "x86". This parameter may be <b>NULL</b>. 



					


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_NOT_ENOUGH_MEMORY, 
<b>SetupSetPlatformPathOverride</b> was unable to store the <i>Override</i> string.




## -remarks



<b>SetPlatformPathOverride</b> is used to change the source path when queuing files. If a platform path override has been set by a call to <b>SetPlatformPathOverride</b>, any setup function that queues file copy operations will examine the final component of the source path and if the final component matches the name of the user's platform, replace it with the override string set by <b>SetPlatformPathOverride</b>.

For example, consider a MIPS-platform machine where the platform has been set to Alpha by a call to <b>SetPlatformPathOverride</b>. After the platform path override has been set, a file copy operation is queued with a source path of \\pop\top\baz\mips\x.exe, the path will be changed to \\pop\top\baz\alpha\x.exe.

The paths of file copy operations queued before the path override is set are not changed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bacb7b90-a391-4f05-bedb-0c0f52fd15f9">SetupSetDirectoryId</a>
 

 

