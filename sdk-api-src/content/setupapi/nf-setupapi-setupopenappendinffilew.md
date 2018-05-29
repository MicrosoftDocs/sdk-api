---
UID: NF:setupapi.SetupOpenAppendInfFileW
title: SetupOpenAppendInfFileW function
author: windows-sdk-content
description: The SetupOpenAppendInfFile function appends the information in an INF file to an INF file previously opened by SetupOpenInfFile.
old-location: setup\setupopenappendinffile.htm
old-project: SetupApi
ms.assetid: 12b1c676-912f-4876-998c-6b0ff162b95d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupOpenAppendInfFile, SetupOpenAppendInfFile function [Setup API], SetupOpenAppendInfFileA, SetupOpenAppendInfFileW, _setupapi_setupopenappendinffile, setup.setupopenappendinffile, setupapi/SetupOpenAppendInfFile, setupapi/SetupOpenAppendInfFileA, setupapi/SetupOpenAppendInfFileW
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
req.unicode-ansi: SetupOpenAppendInfFileW (Unicode) and SetupOpenAppendInfFileA (ANSI)
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
-	SetupOpenAppendInfFile
-	SetupOpenAppendInfFileA
-	SetupOpenAppendInfFileW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupOpenAppendInfFileW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenAppendInfFile</b> function appends the information in an INF file to an INF file previously opened by 
<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>.


## -parameters




### -param FileName [in]

If not <b>NULL</b>, <i>FileName</i> points to a <b>null</b>-terminated string containing the name (and optionally the path) of the INF file to be opened. If the filename does not contain path separator characters, it is searched for, first in the %windir%\inf directory, and then in the %windir%\system32 directory. If the filename contains path separator characters, it is assumed to be a full path specification and no further processing is performed on it. If <i>FileName</i> is <b>NULL</b>, the INF filename is retrieved from the LayoutFile value of the <b>Version</b> section in the existing INF file. The same search logic is applied to the filename retrieved from the LayoutFile key.


### -param InfHandle [in]

Existing INF handle to which this INF file will be appended.


### -param ErrorLine [in, out]

Optional pointer to a variable to which this function returns the (1-based) line number where an error occurred during loading of the INF file. This value is generally reliable only if 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> does not return ERROR_NOT_ENOUGH_MEMORY. If an out-of-memory condition does occur, <i>ErrorLine</i> may be 0.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If <i>FileName</i> was not specified and there was no LayoutFile value in the <b>Version</b> section of the existing INF File, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INVALID_DATA.




## -remarks



This function requires a Windows INF file. Some older INF file  formats may not be supported. In this case, the function returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return ERROR_INVALID_PARAMETER. The main purpose of this function is to combine an INF file with the source file location information contained in the file specified in the LayoutFile entry of the <b>Version</b> section (typically, LAYOUT.INF).

The ERROR_WRONG_INF_STYLE may also be returned by <b>SetupOpenAppendInfFile</b> if the INF file uses an older format.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/78b6a69d-e588-45f1-bf5c-a6feaf8b3364">SetupCloseInfFile</a>



<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>
 

 

