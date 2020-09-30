---
UID: NF:setupapi.SetupDestroyDiskSpaceList
title: SetupDestroyDiskSpaceList function (setupapi.h)
description: The SetupDestroyDiskSpaceList function destroys a disk-space list and releases the resources allocated to it.
helpviewer_keywords: ["SetupDestroyDiskSpaceList","SetupDestroyDiskSpaceList function [Setup API]","_setupapi_setupdestroydiskspacelist","setup.setupdestroydiskspacelist","setupapi/SetupDestroyDiskSpaceList"]
old-location: setup\setupdestroydiskspacelist.htm
tech.root: setup
ms.assetid: bf5fd250-5744-4bb7-ad4f-45f754e75460
ms.date: 12/05/2018
ms.keywords: SetupDestroyDiskSpaceList, SetupDestroyDiskSpaceList function [Setup API], _setupapi_setupdestroydiskspacelist, setup.setupdestroydiskspacelist, setupapi/SetupDestroyDiskSpaceList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDestroyDiskSpaceList
 - setupapi/SetupDestroyDiskSpaceList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDestroyDiskSpaceList
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupcreatediskspacelista">SetupCreateDiskSpaceList</a>