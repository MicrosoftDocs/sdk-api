---
UID: NF:setupapi.SetupCreateDiskSpaceListW
title: SetupCreateDiskSpaceListW function
author: windows-sdk-content
description: The SetupCreateDiskSpaceList function creates a disk-space list.
old-location: setup\setupcreatediskspacelist.htm
old-project: SetupApi
ms.assetid: a578ed9d-12b2-43f4-ab0a-183269de0d40
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupCreateDiskSpaceList, SetupCreateDiskSpaceList function [Setup API], SetupCreateDiskSpaceListA, SetupCreateDiskSpaceListW, _setupapi_setupcreatediskspacelist, setup.setupcreatediskspacelist, setupapi/SetupCreateDiskSpaceList, setupapi/SetupCreateDiskSpaceListA, setupapi/SetupCreateDiskSpaceListW
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
req.unicode-ansi: SetupCreateDiskSpaceListW (Unicode) and SetupCreateDiskSpaceListA (ANSI)
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
 - SetupCreateDiskSpaceList
 - SetupCreateDiskSpaceListA
 - SetupCreateDiskSpaceListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupCreateDiskSpaceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCreateDiskSpaceList</b> function creates a disk-space list.


## -parameters




### -param Reserved1 [in]

Unused, must be zero.


### -param Reserved2 [in]

Unused, must be zero.


### -param Flags [in]

This parameter can be the following value. 







#### SPDSL_IGNORE_DISK

File operations added to the list will ignore files that already exist on the disk. For example, if the disk contains a 5000-byte file, C:\MyDir\MyFile, and you add a Copy operation to the disk-space list for a new version, C:\MyDir\MyFile, that is 6500 bytes, the space required will be 6500 bytes (instead of 1500 bytes, which is the value returned if you do not set SPDSL_IGNORE_DISK).


##### - Flags.SPDSL_IGNORE_DISK

File operations added to the list will ignore files that already exist on the disk. For example, if the disk contains a 5000-byte file, C:\MyDir\MyFile, and you add a Copy operation to the disk-space list for a new version, C:\MyDir\MyFile, that is 6500 bytes, the space required will be 6500 bytes (instead of 1500 bytes, which is the value returned if you do not set SPDSL_IGNORE_DISK).


## -returns



If the function succeeds, it returns a handle to the disk-space list.

If the function fails, it returns null. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bf5fd250-5744-4bb7-ad4f-45f754e75460">SetupDestroyDiskSpaceList</a>
 

 

