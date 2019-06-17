---
UID: NF:setupapi.SetupDuplicateDiskSpaceListA
title: SetupDuplicateDiskSpaceListA function (setupapi.h)
author: windows-sdk-content
description: The SetupDuplicateDiskSpaceList function duplicates a disk-space list as a new independent disk-space list.
old-location: setup\setupduplicatediskspacelist.htm
tech.root: SetupApi
ms.assetid: 92d18c15-e8e2-4e89-8d2f-7c87c948603f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDuplicateDiskSpaceList, SetupDuplicateDiskSpaceList function [Setup API], SetupDuplicateDiskSpaceListA, SetupDuplicateDiskSpaceListW, setup.setupduplicatediskspacelist, setupapi/SetupDuplicateDiskSpaceList, setupapi/SetupDuplicateDiskSpaceListA, setupapi/SetupDuplicateDiskSpaceListW
ms.topic: function
f1_keywords: ["setupapi/SetupDuplicateDiskSpaceList"]
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDuplicateDiskSpaceListW (Unicode) and SetupDuplicateDiskSpaceListA (ANSI)
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
 - SetupDuplicateDiskSpaceList
 - SetupDuplicateDiskSpaceListA
 - SetupDuplicateDiskSpaceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDuplicateDiskSpaceListA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The SetupDuplicateDiskSpaceList function duplicates a disk-space list as a new independent disk-space list.


## -parameters




### -param DiskSpace [in]

Handle to the disk-space list to be duplicated.


### -param Reserved1

Unused, must be  zero.


### -param Reserved2

Unused, must be  zero.


### -param Flags

Unused, must be  zero.


## -returns



If the function succeeds, it returns a handle to the new disk-space list.

If the function fails, it returns null. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>
 

 

