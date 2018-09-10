---
UID: NF:setupapi.SetupOpenInfFileW
title: SetupOpenInfFileW function
author: windows-sdk-content
description: The SetupOpenInfFile function opens an INF file and returns a handle to it.
old-location: setup\setupopeninffile.htm
tech.root: SetupApi
ms.assetid: a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetupOpenInfFile, SetupOpenInfFile function [Setup API], SetupOpenInfFileA, SetupOpenInfFileW, _setupapi_setupopeninffile, setup.setupopeninffile, setupapi/SetupOpenInfFile, setupapi/SetupOpenInfFileA, setupapi/SetupOpenInfFileW
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
req.unicode-ansi: SetupOpenInfFileW (Unicode) and SetupOpenInfFileA (ANSI)
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
 - Ext-MS-Win-setupapi-inf-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
 - SetupOpenInfFile
 - SetupOpenInfFileA
 - SetupOpenInfFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupOpenInfFileW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupOpenInfFile</b> function opens an INF file and returns a handle to it.


## -parameters




### -param FileName [in]

Pointer to a null-terminated string containing the name (and optional path) of the INF file to be opened. If the filename does not contain path separator characters, it is searched for, first in the %windir%\inf directory, and then in the %windir%\system32 directory. If the filename contains path separator characters, it is assumed to be a full path specification and no further processing is performed on it.


### -param InfClass [in]

Optional pointer to a null-terminated string containing the class of INF file desired. This string must match the Class value of the <b>Version</b> section (for example, Class=Net). If there is no entry in the Class value, but there is an entry for ClassGUID in the <b>Version</b> section, the corresponding class name for that GUID is retrieved and used for the comparison. 


### -param InfStyle [in]

Style of INF file to open or search for. This parameter can be a combination of the following flags. 







#### INF_STYLE_OLDNT

A legacy INF file format.



#### INF_STYLE_WIN4

A Windows INF file format.


### -param ErrorLine [in]

Optional pointer to a variable to which this function returns the (1-based) line number where an error occurred during loading of the INF file. This value is generally reliable only if 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> does not return ERROR_NOT_ENOUGH_MEMORY. If an out-of-memory condition does occur, <i>ErrorLine</i> may be 0.


##### - InfStyle.INF_STYLE_OLDNT

A legacy INF file format.


##### - InfStyle.INF_STYLE_WIN4

A Windows INF file format.


## -returns



The function returns a handle to the opened INF file if it is successful. Otherwise, the return value is INVALID_HANDLE_VALUE. Extended error information can be retrieved by a call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the load fails because the INF file type does not match <i>InfClass</i>, the function returns INVALID_HANDLE_VALUE and a call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_CLASS_MISMATCH.

If multiple INF file styles are specified, the style of the INF file opened can be determined by calling the 
<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a> function.

Because there may be more than one class GUID with the same class name, callers interested in INF files of a particular class (that is, a particular class GUID) should retrieve the ClassGUID value from the INF file by calling 
<a href="https://msdn.microsoft.com/58768b91-a0c7-4791-8667-2890b742798c">SetupQueryInfVersionInformation</a>.

For legacy INF files, the <i>InfClass</i> string must match the type specified in the OptionType value of the <b>Identification</b> section in the INF file (for example, OptionType=NetAdapter).




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/78b6a69d-e588-45f1-bf5c-a6feaf8b3364">SetupCloseInfFile</a>



<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a>



<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>
 

 

