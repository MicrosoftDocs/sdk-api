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

# SetupSetDirectoryIdExW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetDirectoryIdEx</b> function associates a directory identifier in an INF file with a specific directory.


## -parameters




### -param InfHandle [in]

A handle for a loaded INF file.


### -param Id [in]

A directory identifier (DIRID) to use for an association. This parameter can be <b>NULL</b>. This DIRID must be greater than or equal to DIRID_USER. If an association already exists for this DIRID, it is overwritten. If <i>Id</i> is zero, the <i>Directory</i> parameter is ignored, and the current set of user-defined DIRIDs is deleted.


### -param Directory [in]

A pointer to  a <b>null</b>-terminated string that specifies the directory path to associate with <i>Id</i>. This parameter can be <b>NULL</b>. If <i>Directory</i> is <b>NULL</b>, any directory associated with <i>Id</i> is unassociated. No error results if <i>Id</i> is not currently associated with a directory.


### -param Flags [in]

This parameter can be set to <b>SETDIRID_NOT_FULL_PATH</b> (1) to indicate that the <i>Directory</i> does not specify a full path.


### -param Reserved1

If the value of this parameter is not zero the function returns  ERROR_INVALID_PARAMETER.


### -param Reserved2

If the value of this parameter is not zero the function returns  ERROR_INVALID_PARAMETER.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SetupSetDirectoryIdEx</b> can be used prior to queuing file copy operations to specify a target location that is only known at runtime.

After setting the directory identifier, this function traverses all appended INF files, and if any of them have unresolved string substitutions, the function attempts to re-apply string substitution to them based on the new DIRID mapping. Because of this, some INF values may change after calling 
<b>SetupSetDirectoryIdEx</b>.

DIRID_ABSOLUTE_16BIT is not a valid value for <i>Id</i>, which ensures compatibility with 16-bit setup.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

