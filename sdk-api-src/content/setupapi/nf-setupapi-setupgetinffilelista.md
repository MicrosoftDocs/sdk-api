---
UID: NF:setupapi.SetupGetInfFileListA
title: SetupGetInfFileListA function
author: windows-driver-content
description: The SetupGetInfFileList function returns a list of INF files located in a caller-specified directory to a call-supplied buffer.
old-location: setup\setupgetinffilelist.htm
old-project: SetupApi
ms.assetid: d7074e88-757c-4ca9-adaf-2010472f106c
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: SetupGetInfFileList, SetupGetInfFileList function [Setup API], SetupGetInfFileListA, SetupGetInfFileListW, _setupapi_setupgetinffilelist, setup.setupgetinffilelist, setupapi/SetupGetInfFileList, setupapi/SetupGetInfFileListA, setupapi/SetupGetInfFileListW
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
req.unicode-ansi: SetupGetInfFileListW (Unicode) and SetupGetInfFileListA (ANSI)
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
-	SetupGetInfFileList
-	SetupGetInfFileListA
-	SetupGetInfFileListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupGetInfFileListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetInfFileList</b> function returns a list of INF files located in a caller-specified directory to a call-supplied buffer.


## -parameters




### -param DirectoryPath [in]

Optional pointer to a <b>null</b>-terminated string containing the path of the directory in which to search. If this value is <b>NULL</b>, the %windir%\inf directory is used.


### -param InfStyle [in]

Type of INF file to search for. May be a combination of the following flags. 







#### INF_STYLE_OLDNT

A legacy INF file format.



#### INF_STYLE_WIN4

A Windows INF file format.


### -param ReturnBuffer [in, out]

 If not <b>NULL</b>, points to a buffer in which this function returns the list of all INF files of the desired styles that were found in the specified subdirectory. File names are <b>null</b>-terminated, with an extra <b>null</b> at the end of the list. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size. The filenames do not include the path. See the Remarks section.
 



### -param ReturnBufferSize [in]

Size of the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is not specified, <i>ReturnBufferSize</i> is ignored. 



### -param RequiredSize [in, out]

If not <b>NULL</b>, points to a variable in which this function returns the required size for the buffer pointed to by the <i>ReturnBuffer</i> parameter, in characters. This includes the <b>null</b> terminator. If <i>ReturnBuffer</i> is specified and the size needed is larger than <i>ReturnBufferSize</i>, the function fails and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER.



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a ReturnBuffer of <b>NULL</b> and a <i>ReturnBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>RequiredSize</i>. If the function succeeds in this, the return value is a nonzero value. Otherwise, the return value is zero and extended error information can be obtained by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


If multiple INF file styles are returned by this function, the style of a particular INF file can be determined by calling the <a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a> function




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a>
 

 

