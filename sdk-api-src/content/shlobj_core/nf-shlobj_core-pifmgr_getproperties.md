---
UID: NF:shlobj_core.PifMgr_GetProperties
title: PifMgr_GetProperties function
author: windows-sdk-content
description: Returns a specified block of data from a .pif file.
old-location: properties\PifMgr_GetProperties.htm
tech.root: properties
ms.assetid: 62933ddf-9b0d-427a-8b5f-a0117a3b4885
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PifMgr_GetProperties, PifMgr_GetProperties function [Windows Properties], _win32_PifMgr_GetProperties, properties.PifMgr_GetProperties, shell.PifMgr_GetProperties, shlobj_core/PifMgr_GetProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PifMgr_GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PifMgr_GetProperties function


## -description


<p class="CCE_Message">[<b>PifMgr_GetProperties</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Returns a specified block of data from a .pif file.


## -parameters




### -param hProps [in, optional]

Type: <b>HANDLE</b>

A handle to an application's properties. This parameter should be set to the value that is returned by <a href="https://msdn.microsoft.com/0bc11528-7278-4765-b3cb-671ba82c9155">PifMgr_OpenProperties</a>.


### -param pszGroup [in, optional]

Type: <b>PCSTR</b>

A null-terminated string that contains the property group name. It can be one of the following, or any other name that corresponds to a valid .pif extension.



#### 

"WINDOWS 286 3.0"

"WINDOWS 386 3.0"

"WINDOWS VMM 4.0"

"WINDOWS NT  3.1"

"WINDOWS NT  4.0"


### -param lpProps [out, optional]

Type: <b>void*</b>

When this function returns, contains a pointer to a <a href="https://msdn.microsoft.com/603f990b-efb8-4d72-bc96-27bda4ffcbd8">PROPPRG</a> structure.


### -param cbProps

Type: <b>int</b>

The size of the buffer, in bytes, pointed to by <i>lpProps</i>.


### -param flOpt

Type: <b>UINT</b>

Set this parameter to GETPROPS_NONE.


## -returns



Type: <b>int</b>

Returns <b>NULL</b> if successful. If unsuccessful, the function returns the handle to the application properties that were passed as <i>hProps</i>.




## -remarks



If the block is a "named" block, it must be the name of a linked extension inside the .pif file. This can be any predefined name (such as, "WINDOWS 386 3.0") or the name of your own block. You can create your own named data blocks using <a href="https://msdn.microsoft.com/720ed580-1867-4651-aef6-24ac4397ad39">PifMgr_SetProperties</a>. Named data can also be thought of as raw data, because it is returned to the calling application as it is, without translation.

The size of a named block can be determined by calling <b>PifMgr_GetProperties</b> with <i>cbProps</i> set to 0. No data is copied, but the size of the requested block is returned.

All named blocks can be enumerated by setting <i>pszGroup</i> to <b>NULL</b>. <i>lpProps</i> must be a pointer to a 16-byte buffer to contain the requested block name, and <i>cbProps</i> must be set to the zero-based block index.  The return value is the size of the block, or zero if the block is not found.

If you request an unnamed property block by setting the selector of the name parameter to <b>NULL</b>, and the offset is a property group ordinal, then the associated structure is returned. For example, PifMgr_GetProperties(GROUP_TSK) returns a predefined structure that contains all the task-related information in a format that is independent of the .pif file. This is a valuable service because it relieves calling applications from dealing with .pif files that contain a wide variety of sections (known as .pif extensions), when only one is required.




## -see-also




<a href="https://msdn.microsoft.com/fd50d4f8-87c8-4162-9e88-3c8592b929fa">PifMgr_CloseProperties</a>



<a href="https://msdn.microsoft.com/0bc11528-7278-4765-b3cb-671ba82c9155">PifMgr_OpenProperties</a>
 

 

