---
UID: NF:shobjidl_core.IFileSystemBindData.GetFindData
title: IFileSystemBindData::GetFindData (shobjidl_core.h)
description: Gets the file system information stored in the WIN32_FIND_DATA structure.
helpviewer_keywords: ["GetFindData","GetFindData method [Windows Shell]","GetFindData method [Windows Shell]","IFileSystemBindData interface","IFileSystemBindData interface [Windows Shell]","GetFindData method","IFileSystemBindData.GetFindData","IFileSystemBindData::GetFindData","_shell_ifilesystembinddata_getfinddata","shell.IFileSystemBindData_GetFindData","shobjidl_core/IFileSystemBindData::GetFindData"]
old-location: shell\IFileSystemBindData_GetFindData.htm
tech.root: shell
ms.assetid: 75161b45-42b9-4d64-ae13-583d07920a0b
ms.date: 12/05/2018
ms.keywords: GetFindData, GetFindData method [Windows Shell], GetFindData method [Windows Shell],IFileSystemBindData interface, IFileSystemBindData interface [Windows Shell],GetFindData method, IFileSystemBindData.GetFindData, IFileSystemBindData::GetFindData, _shell_ifilesystembinddata_getfinddata, shell.IFileSystemBindData_GetFindData, shobjidl_core/IFileSystemBindData::GetFindData
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemBindData::GetFindData
 - shobjidl_core/IFileSystemBindData::GetFindData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSystemBindData.GetFindData
---

# IFileSystemBindData::GetFindData


## -description

Gets the file system information stored in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.

## -parameters

### -param pfd [out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>*</b>

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that receives the data.

## -returns

Type: <b>HRESULT</b>

Returns S_OK.

## -remarks

This method provides bind context information to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a>. The client accesses the object by calling <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam">IBindCtx::GetObjectParam</a> with the <i>pszKey</i> parameter set to the string "File System Bind Data".