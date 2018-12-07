---
UID: NF:shlobj_core.IACList2.GetOptions
title: IACList2::GetOptions
author: windows-sdk-content
description: Gets the current autocomplete options.
old-location: shell\IACList2_GetOptions.htm
tech.root: shell
ms.assetid: 767c1972-8bc8-46d5-abf0-8c5749c0bf0e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ACLO_CURRENTDIR, ACLO_DESKTOP, ACLO_FAVORITES, ACLO_FILESYSDIRS, ACLO_FILESYSONLY, ACLO_MYCOMPUTER, ACLO_NONE, GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IACList2 interface, IACList2 interface [Windows Shell],GetOptions method, IACList2.GetOptions, IACList2::GetOptions, _win32_IACList2_GetOptions, shell.IACList2_GetOptions, shlobj_core/IACList2::GetOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IACList2.GetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IACList2::GetOptions


## -description


Gets the current autocomplete options.


## -parameters




### -param pdwFlag [out]

Type: <b>DWORD*</b>

A pointer to a value that will hold the current option flag when the method returns. This can be a combination of the following values.



#### ACLO_CURRENTDIR

Enumerate the current working directory.



#### ACLO_DESKTOP

Enumerate the Desktop folder.



#### ACLO_FAVORITES

Enumerate the Favorites folder.



#### ACLO_FILESYSONLY

Enumerate only items that are part of the file system. Do not enumerate items contained by virtual folders.



#### ACLO_FILESYSDIRS

Enumerate only the file system directories, UNC shares, and UNC servers.



#### ACLO_MYCOMPUTER

Enumerate the My Computer folder.



#### ACLO_NONE

Do not enumerate anything.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/b765c9dd-20e9-428f-877a-aff4fac44664">IACList2</a>
 

 

