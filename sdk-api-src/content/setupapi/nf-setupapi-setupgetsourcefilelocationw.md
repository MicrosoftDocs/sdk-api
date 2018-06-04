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

# SetupGetSourceFileLocationW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetSourceFileLocation</b> function retrieves the location of a source file listed in an INF file.


## -parameters




### -param InfHandle [in]

Handle to the INF file that contains the <b>SourceDisksNames</b> and <b>SourceDisksFiles</b> sections. If platform-specific sections exist for the user's system (for example, <b>SourceDisksNames.x86</b> and <b>SourceDisksFiles.x86</b>), the platform-specific section will be used.


### -param InfContext [in]

Optional pointer to the context of a line in a <b>Copy Files</b> section for which the full source path is to be retrieved. If this parameter is <b>NULL</b>, <i>FileName</i> is searched for in the <b>SourceDisksFiles</b> section of the INF file specified by <i>InfHandle</i>.


### -param FileName [in]

Optional pointer to a <b>null</b>-terminated string containing the filename (no path) for which to return the full source location. This parameter can be <b>NULL</b>, but either <i>FileName</i> or <i>InfContext</i> must be specified. 



### -param SourceId [in, out]

Pointer to a variable that receives the source identifier of the media where the file is located from the <b>SourceDisksNames</b> section of the INF file.


### -param ReturnBuffer [in, out]

 Optional pointer to a buffer to receive the relative source path. The source path does not include the filename itself, nor does it include a drive letter/network share name. The path does not start or end with a backslash (\), so the empty string specifies the root directory. You should use a <b>null</b>-terminated string buffer. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data.  Using this technique, you can avoid errors due to an insufficient buffer size. See the Remarks section. This parameter can be <b>NULL</b>.



### -param ReturnBufferSize [out]

Size of the buffer pointed to by <i>ReturnBuffer</i>, in characters. This number includes the <b>null</b> terminator. 



### -param RequiredSize [in, out]

Optional pointer to a variable that receives the required size for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This number includes the <b>null</b> terminator. If the required size is larger than the value specified by <i>ReturnBufferSize</i>, the function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>ReturnBuffer</i> of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/f1db8ad5-b133-410e-9843-38b09e2ef5e7">SetupGetSourceFileSize</a>



<a href="https://msdn.microsoft.com/15bedd7f-7079-4623-a797-db308a51093f">SetupGetSourceInfo</a>
 

 

