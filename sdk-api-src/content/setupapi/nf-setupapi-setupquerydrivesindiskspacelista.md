---
UID: NF:setupapi.SetupQueryDrivesInDiskSpaceListA
title: SetupQueryDrivesInDiskSpaceListA function
author: windows-sdk-content
description: The SetupQueryDrivesInDiskSpaceList function fills a buffer with a list of the drives referenced by the file operations listed in the disk-space list.
old-location: setup\setupquerydrivesindiskspacelist.htm
tech.root: SetupApi
ms.assetid: be298b54-f5dc-46a3-a54c-f7ca5cb3a2fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupQueryDrivesInDiskSpaceList, SetupQueryDrivesInDiskSpaceList function [Setup API], SetupQueryDrivesInDiskSpaceListA, SetupQueryDrivesInDiskSpaceListW, _setupapi_setupquerydrivesindiskspacelist, setup.setupquerydrivesindiskspacelist, setupapi/SetupQueryDrivesInDiskSpaceList, setupapi/SetupQueryDrivesInDiskSpaceListA, setupapi/SetupQueryDrivesInDiskSpaceListW
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
req.unicode-ansi: SetupQueryDrivesInDiskSpaceListW (Unicode) and SetupQueryDrivesInDiskSpaceListA (ANSI)
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
 - SetupQueryDrivesInDiskSpaceList
 - SetupQueryDrivesInDiskSpaceListA
 - SetupQueryDrivesInDiskSpaceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupQueryDrivesInDiskSpaceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryDrivesInDiskSpaceList</b> function fills a buffer with a list of the drives referenced by the file operations listed in the disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to the disk-space list.


### -param ReturnBuffer [in, out]

Optional pointer to a buffer that receives the drive specifications, such as "X:" or "\\server\share". You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. This parameter can be <b>NULL</b>.
If this parameter is not specified and no error occurs, the function returns a nonzero value and <i>RequiredSize</i> receives the buffer size required to hold the drive specifications. 

					


### -param ReturnBufferSize [in]

Size of the buffer pointed by <i>ReturnBuffer</i>, in characters. This includes the <b>null</b> terminator. This parameter is ignored if <i>ReturnBuffer</i> is not specified. 



### -param RequiredSize [in, out]

Optional pointer to a variable that receives the size of the buffer required to hold the <b>null</b>-terminated list of drives, in characters. This includes the <b>null</b> terminator. 


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns ERROR_INSUFFICIENT_BUFFER, <i>ReturnBuffer</i> was specified, but <i>ReturnBufferSize</i> indicated that the supplied buffer was too small.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/529e04e2-671a-4aad-bb1c-2b24cf2e5cd1">SetupQuerySpaceRequiredOnDrive</a>
 

 

