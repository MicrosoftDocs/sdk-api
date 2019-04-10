---
UID: NF:setupapi.SetupAdjustDiskSpaceListA
title: SetupAdjustDiskSpaceListA function (setupapi.h)
author: windows-sdk-content
description: The SetupAdjustDiskSpaceList function adjusts the amount of required space for a specified drive.
old-location: setup\setupadjustdiskspacelist.htm
tech.root: SetupApi
ms.assetid: dcdcc43c-9b5c-495b-bf4b-331c4d9461e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupAdjustDiskSpaceList, SetupAdjustDiskSpaceList function [Setup API], SetupAdjustDiskSpaceListA, SetupAdjustDiskSpaceListW, setup.setupadjustdiskspacelist, setupapi/SetupAdjustDiskSpaceList, setupapi/SetupAdjustDiskSpaceListA, setupapi/SetupAdjustDiskSpaceListW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupAdjustDiskSpaceListW (Unicode) and SetupAdjustDiskSpaceListA (ANSI)
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
 - SetupAdjustDiskSpaceList
 - SetupAdjustDiskSpaceListA
 - SetupAdjustDiskSpaceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupAdjustDiskSpaceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupAdjustDiskSpaceList</b> function adjusts the amount of required space for a specified drive.


## -parameters




### -param DiskSpace [in]

Handle to a disk-space list.


### -param DriveRoot [in]

Specifies a valid Win32 drive root. An entry is added to the disk-space list if the specified drive is not currently in the disk-space list.  


### -param Amount [in]

Specifies the amount of space to add or remove. Use a negative number to remove space and use a positive number to add space.


### -param Reserved1

Unused, must be  zero.


### -param Reserved2

Unused, must be  zero.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

