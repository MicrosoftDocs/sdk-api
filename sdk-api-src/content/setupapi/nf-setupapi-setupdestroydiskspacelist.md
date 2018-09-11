---
UID: NF:setupapi.SetupDestroyDiskSpaceList
title: SetupDestroyDiskSpaceList function
author: windows-sdk-content
description: The SetupDestroyDiskSpaceList function destroys a disk-space list and releases the resources allocated to it.
old-location: setup\setupdestroydiskspacelist.htm
tech.root: SetupApi
ms.assetid: bf5fd250-5744-4bb7-ad4f-45f754e75460
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetupDestroyDiskSpaceList, SetupDestroyDiskSpaceList function [Setup API], _setupapi_setupdestroydiskspacelist, setup.setupdestroydiskspacelist, setupapi/SetupDestroyDiskSpaceList
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
req.unicode-ansi: 
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
 - SetupDestroyDiskSpaceList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDestroyDiskSpaceList function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupDestroyDiskSpaceList</b> function destroys a disk-space list and releases the resources allocated to it.


## -parameters




### -param DiskSpace [in, out]

Handle to the disk-space list to be deconstructed.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/a578ed9d-12b2-43f4-ab0a-183269de0d40">SetupCreateDiskSpaceList</a>
 

 

