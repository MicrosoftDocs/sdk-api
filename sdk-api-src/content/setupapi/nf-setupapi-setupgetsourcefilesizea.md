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

# SetupGetSourceFileSizeA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetSourceFileSize</b> function reads the uncompressed size of a source file listed in an INF file.


## -parameters




### -param InfHandle [in]

Handle to the loaded INF file that contains the <b>SourceDisksNames</b> and <b>SourceDisksFiles</b> sections. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b> and <b>SourceDisksFiles.x86</b>), the platform-specific section will be used.


### -param InfContext [in]

Optional pointer to a context for a line in a <b>Copy Files</b> section for which the size is to be retrieved. If <i>InfContext</i> is <b>NULL</b>, the <i>FileName</i> parameter is used.


### -param FileName [in]

Optional pointer to a <b>null</b>-terminated string containing the filename (no path) for which to return the size. If this parameter is <b>NULL</b> as well as <i>InfContext</i>, then the <i>Section</i> parameter is used.


### -param Section [in]

Optional pointer to a <b>null</b>-terminated string containing the name of a <b>Copy Files</b> section. If this parameter is specified, the total size of all files listed in the section is computed.


### -param FileSize [in, out]

Pointer to a variable that receives the size, in bytes, of the specified file(s).


### -param RoundingFactor [in]

Optional value for rounding file sizes. All file sizes are rounded up to a multiple of this number before being added to the total size. Rounding is useful for more exact determinations of the space that a file will occupy on a given volume, because it allows the caller to have file sizes rounded up to a multiple of the cluster size. Rounding does not occur unless <i>RoundingFactor</i> is specified.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



One and only one of the optional parameters, <i>InfContext</i>, <i>FileName</i>, and <i>Section</i>, must be specified.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/00245cb9-99de-464a-a0b4-d1efb1f1331b">SetupGetSourceFileLocation</a>
 

 

