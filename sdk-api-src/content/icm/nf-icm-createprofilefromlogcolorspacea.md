---
UID: NF:icm.CreateProfileFromLogColorSpaceA
title: CreateProfileFromLogColorSpaceA function
author: windows-sdk-content
description: The CreateProfileFromLogColorSpace function converts a logical color space to a device profile.
old-location: wcs\createprofilefromlogcolorspace.htm
tech.root: WCS
ms.assetid: ac2fddd4-ac93-49a8-883a-cf888b542812
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateProfileFromLogColorSpace, CreateProfileFromLogColorSpace function [Windows Color System], CreateProfileFromLogColorSpaceA, CreateProfileFromLogColorSpaceW, _color_CreateProfileFromLogColorSpace, icm/CreateProfileFromLogColorSpace, icm/CreateProfileFromLogColorSpaceA, icm/CreateProfileFromLogColorSpaceW, wcs.createprofilefromlogcolorspace
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
req.unicode-ansi: CreateProfileFromLogColorSpaceW (Unicode) and CreateProfileFromLogColorSpaceA (ANSI)
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
 - CreateProfileFromLogColorSpace
 - CreateProfileFromLogColorSpaceA
 - CreateProfileFromLogColorSpaceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateProfileFromLogColorSpaceA function


## -description


The <b>CreateProfileFromLogColorSpace</b> function converts a logical <a href="c.htm">color space</a> to a <a href="d.htm">device profile</a>.


## -parameters




### -param pLogColorSpace

A pointer to a logical color space structure. See <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a> for details. The <b>lcsFilename</b> [0] member of the structure must be set to the <b>null</b> character ('\0') or this function call will fail with the return value of INVALID_PARAMETER.


### -param pProfile

TBD




#### - pBuffer

A pointer to a pointer to a buffer where the device profile will be created. This function allocates the buffer and fills it with profile information if it is successful. If not, the pointer is set to <b>NULL</b>. The caller is responsible for freeing this buffer when it is no longer needed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

If the <b>lcsFilename</b> [0] member if the <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a> structure pointed to by <i>pLogColorSpace</i> is not '\0', this function returns INVALID_PARAMETER.




## -remarks



This function can be used with ASCII or Unicode strings. The buffer created by this function must be freed by the caller when it is no longer needed or there will be a memory leak. The <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function should be used to free this buffer.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>
 

 

