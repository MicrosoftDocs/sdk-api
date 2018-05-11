---
UID: NF:setupapi.SetupDuplicateDiskSpaceListA
title: SetupDuplicateDiskSpaceListA function
author: windows-driver-content
description: The SetupDuplicateDiskSpaceList function duplicates a disk-space list as a new independent disk-space list.
old-location: setup\setupduplicatediskspacelist.htm
old-project: SetupApi
ms.assetid: 92d18c15-e8e2-4e89-8d2f-7c87c948603f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupDuplicateDiskSpaceList, SetupDuplicateDiskSpaceList function [Setup API], SetupDuplicateDiskSpaceListA, SetupDuplicateDiskSpaceListW, setup.setupduplicatediskspacelist, setupapi/SetupDuplicateDiskSpaceList, setupapi/SetupDuplicateDiskSpaceListA, setupapi/SetupDuplicateDiskSpaceListW
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
req.unicode-ansi: SetupDuplicateDiskSpaceListW (Unicode) and SetupDuplicateDiskSpaceListA (ANSI)
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
-	SetupDuplicateDiskSpaceList
-	SetupDuplicateDiskSpaceListA
-	SetupDuplicateDiskSpaceListW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

