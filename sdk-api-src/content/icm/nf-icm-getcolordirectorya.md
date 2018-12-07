---
UID: NF:icm.GetColorDirectoryA
title: GetColorDirectoryA function
author: windows-sdk-content
description: The GetColorDirectory function retrieves the path of the Windows COLOR directory on a specified machine.
old-location: wcs\getcolordirectory.htm
tech.root: WCS
ms.assetid: 9e26e58b-0497-4879-963c-fae91f5740bf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetColorDirectory, GetColorDirectory function [Windows Color System], GetColorDirectoryA, GetColorDirectoryW, _color_GetColorDirectory, icm/GetColorDirectory, icm/GetColorDirectoryA, icm/GetColorDirectoryW, wcs.getcolordirectory
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
req.unicode-ansi: GetColorDirectoryW (Unicode) and GetColorDirectoryA (ANSI)
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
 - GetColorDirectory
 - GetColorDirectoryA
 - GetColorDirectoryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetColorDirectoryA
: 
---

# GetColorDirectoryA function


## -description


The <b>GetColorDirectory</b> function retrieves the path of the Windows COLOR directory on a specified machine.


## -parameters




### -param pMachineName

Reserved; must be <b>NULL</b>. This parameter is intended to point to the name of the machine on which the profile is to be installed. A <b>NULL</b> pointer indicates the local machine.


### -param pBuffer

Points to the buffer in which the color directory path is to be placed.


### -param pdwSize

Points to a variable containing the size in bytes of the buffer pointed to by <i>pBuffer</i>. On return, the variable contains the size of the buffer actually used or needed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



<b>Per-user/LUA support</b>

Color directory is still system wide. This function is executable in LUA context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

