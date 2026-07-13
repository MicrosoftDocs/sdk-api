---
UID: NF:shobjidl_core.IShellLinkW.GetPath
title: IShellLinkW::GetPath (shobjidl_core.h)
description: Gets the path and file name of the target of a Shell link object. (Unicode)
helpviewer_keywords: ["GetPath","GetPath method [Windows Shell]","GetPath method [Windows Shell]","IShellLink interface","GetPath method [Windows Shell]","IShellLinkA interface","GetPath method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetPath method","IShellLink::GetPath","IShellLinkA interface [Windows Shell]","GetPath method","IShellLinkA::GetPath","IShellLinkW interface [Windows Shell]","GetPath method","IShellLinkW.GetPath","IShellLinkW::GetPath","SLGP_RAWPATH","SLGP_RELATIVEPRIORITY","SLGP_SHORTPATH","SLGP_UNCPRIORITY","_win32_IShellLink_GetPath","shell.IShellLink_GetPath","shobjidl_core/IShellLink::GetPath","shobjidl_core/IShellLinkA::GetPath","shobjidl_core/IShellLinkW::GetPath"]
old-location: shell\IShellLink_GetPath.htm
tech.root: shell
ms.assetid: 7c60f5a2-dc21-4b13-a201-1fab04c53bb4
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [Windows Shell], GetPath method [Windows Shell],IShellLink interface, GetPath method [Windows Shell],IShellLinkA interface, GetPath method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetPath method, IShellLink::GetPath, IShellLinkA interface [Windows Shell],GetPath method, IShellLinkA::GetPath, IShellLinkW interface [Windows Shell],GetPath method, IShellLinkW.GetPath, IShellLinkW::GetPath, SLGP_RAWPATH, SLGP_RELATIVEPRIORITY, SLGP_SHORTPATH, SLGP_UNCPRIORITY, _win32_IShellLink_GetPath, shell.IShellLink_GetPath, shobjidl_core/IShellLink::GetPath, shobjidl_core/IShellLinkA::GetPath, shobjidl_core/IShellLinkW::GetPath
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkW::GetPath
 - shobjidl_core/IShellLinkW::GetPath
dev_langs:
 - c++
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
---

# IShellLinkW::GetPath


## -description

Gets the path and file name of the target of a Shell link object.

## -parameters

### -param pszFile [out]

Type: <b>LPTSTR</b>

The address of a buffer that receives the path and file name of the target of the Shell link object.

### -param cch [in]

Type: <b>int</b>

The size, in characters, of the buffer pointed to by the <i>pszFile</i> parameter, including the terminating null character. The maximum path size that can be returned is MAX_PATH. This parameter is commonly set by calling ARRAYSIZE(pszFile). The ARRAYSIZE macro is defined in Winnt.h.

### -param pfd [in, out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>*</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that receives information about the target of the Shell link object. If this parameter is <b>NULL</b>, then no additional information is returned.

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

<b>Windows Vista and later</b>. Retrieves the path, if possible, of the shortcut's target relative to the path set by a previous call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setrelativepath">IShellLink::SetRelativePath</a>.


##### - fFlags.SLGP_RAWPATH

Retrieves the raw path name. A raw path is something that might not exist and may include environment variables that need to be expanded.


##### - fFlags.SLGP_RELATIVEPRIORITY

<b>Windows Vista and later</b>. Retrieves the path, if possible, of the shortcut's target relative to the path set by a previous call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setrelativepath">IShellLink::SetRelativePath</a>.


##### - fFlags.SLGP_SHORTPATH

Retrieves the standard short (8.3 format) file name.


##### - fFlags.SLGP_UNCPRIORITY

Unsupported; do not use.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the operation is successful and a valid path is retrieved. If the operation is successful but no path is retrieved, it returns <b>S_FALSE</b> and <i>pszFile</i> will be empty. Otherwise, it returns one of the standard HRESULT error values.
