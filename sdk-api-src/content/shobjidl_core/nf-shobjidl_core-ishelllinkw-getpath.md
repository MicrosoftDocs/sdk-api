---
UID: NF:shobjidl_core.IShellLinkW.GetPath
title: IShellLinkW::GetPath
author: windows-sdk-content
description: Gets the path and file name of the target of a Shell link object.
old-location: shell\IShellLink_GetPath.htm
tech.root: shell
ms.assetid: 7c60f5a2-dc21-4b13-a201-1fab04c53bb4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetPath, GetPath method [Windows Shell], GetPath method [Windows Shell],IShellLink interface, GetPath method [Windows Shell],IShellLinkA interface, GetPath method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetPath method, IShellLink::GetPath, IShellLinkA interface [Windows Shell],GetPath method, IShellLinkA::GetPath, IShellLinkW interface [Windows Shell],GetPath method, IShellLinkW.GetPath, IShellLinkW::GetPath, SLGP_RAWPATH, SLGP_RELATIVEPRIORITY, SLGP_SHORTPATH, SLGP_UNCPRIORITY, _win32_IShellLink_GetPath, shell.IShellLink_GetPath, shobjidl_core/IShellLink::GetPath, shobjidl_core/IShellLinkA::GetPath, shobjidl_core/IShellLinkW::GetPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink.GetPath
 - IShellLinkA.GetPath
 - IShellLinkW.GetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkW::GetPath


## -description


Gets the path and file name of the target of a Shell link object.


## -parameters




### -param pszFile [out]

Type: <b>LPTSTR</b>

The address of a buffer that receives the path and file name of the target of the Shell link object.


### -param cch

TBD


### -param pfd [in, out]

Type: <b><a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure that receives information about the target of the Shell link object. If this parameter is <b>NULL</b>, then no additional information is returned.


### -param fFlags [in]

Type: <b>DWORD</b>

Flags that specify the type of path information to retrieve. This parameter can be a combination of the following values.



#### SLGP_SHORTPATH

Retrieves the standard short (8.3 format) file name.



#### SLGP_UNCPRIORITY

Unsupported; do not use.



#### SLGP_RAWPATH

Retrieves the raw path name. A raw path is something that might not exist and may include environment variables that need to be expanded.



#### SLGP_RELATIVEPRIORITY

<b>Windows Vista and later</b>. Retrieves the path, if possible, of the shortcut's target relative to the path set by a previous call to <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">IShellLink::SetRelativePath</a>.


#### - cchMaxPath [in]

Type: <b>int</b>

The size, in characters, of the buffer pointed to by the <i>pszFile</i> parameter, including the terminating null character. The maximum path size that can be returned is MAX_PATH. This parameter is commonly set by calling ARRAYSIZE(pszFile). The ARRAYSIZE macro is defined in Winnt.h.


##### - fFlags.SLGP_RAWPATH

Retrieves the raw path name. A raw path is something that might not exist and may include environment variables that need to be expanded.


##### - fFlags.SLGP_RELATIVEPRIORITY

<b>Windows Vista and later</b>. Retrieves the path, if possible, of the shortcut's target relative to the path set by a previous call to <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">IShellLink::SetRelativePath</a>.


##### - fFlags.SLGP_SHORTPATH

Retrieves the standard short (8.3 format) file name.


##### - fFlags.SLGP_UNCPRIORITY

Unsupported; do not use.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the operation is successful and a valid path is retrieved. If the operation is successful but no path is retrieved, it returns <b>S_FALSE</b> and <i>pszFile</i> will be empty. Otherwise, it returns one of the standard HRESULT error values.



