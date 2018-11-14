---
UID: NF:icm.InstallColorProfileA
title: InstallColorProfileA function
author: windows-sdk-content
description: The InstallColorProfile function installs a given profile for use on a specified machine. The profile is also copied to the COLOR directory.
old-location: wcs\installcolorprofile.htm
tech.root: WCS
ms.assetid: 494b2080-a0a8-4fda-bc12-3bf196a6840c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: InstallColorProfile, InstallColorProfile function [Windows Color System], InstallColorProfileA, InstallColorProfileW, _color_InstallColorProfile, icm/InstallColorProfile, icm/InstallColorProfileA, icm/InstallColorProfileW, wcs.installcolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InstallColorProfileW (Unicode) and InstallColorProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - InstallColorProfile
 - InstallColorProfileA
 - InstallColorProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- InstallColorProfileA
: 
---

# InstallColorProfileA function


## -description


The <b>InstallColorProfile</b> function installs a given profile for use on a specified machine. The profile is also copied to the COLOR directory.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the computer on which the profile is to be installed. A <b>NULL</b> pointer indicates the local computer.


### -param pProfileName

Pointer to the fully qualified path name of the profile to install.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

