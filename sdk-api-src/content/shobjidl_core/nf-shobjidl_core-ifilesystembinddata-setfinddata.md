---
UID: NF:shobjidl_core.IFileSystemBindData.SetFindData
title: IFileSystemBindData::SetFindData (shobjidl_core.h)
description: Stores file system information in a WIN32_FIND_DATA structure. This information is used by ParseDisplayName.
helpviewer_keywords: ["IFileSystemBindData interface [Windows Shell]","SetFindData method","IFileSystemBindData.SetFindData","IFileSystemBindData::SetFindData","SetFindData","SetFindData method [Windows Shell]","SetFindData method [Windows Shell]","IFileSystemBindData interface","_shell_ifilesystembinddata_setfinddata","shell.IFileSystemBindData_SetFindData","shobjidl_core/IFileSystemBindData::SetFindData"]
old-location: shell\IFileSystemBindData_SetFindData.htm
tech.root: shell
ms.assetid: 8e2af85f-5eca-46e4-b193-bf25e2366fac
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData interface [Windows Shell],SetFindData method, IFileSystemBindData.SetFindData, IFileSystemBindData::SetFindData, SetFindData, SetFindData method [Windows Shell], SetFindData method [Windows Shell],IFileSystemBindData interface, _shell_ifilesystembinddata_setfinddata, shell.IFileSystemBindData_SetFindData, shobjidl_core/IFileSystemBindData::SetFindData
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
 - IFileSystemBindData::SetFindData
 - shobjidl_core/IFileSystemBindData::SetFindData
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
 - IFileSystemBindData.SetFindData
---

# IFileSystemBindData::SetFindData


## -description

Stores file system information in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure. This information is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">ParseDisplayName</a>.

## -parameters

### -param pfd [in]

Type: <b>const <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>*</b>

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure that specifies the data you want to store.

## -returns

Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.

## -remarks

After the client stores the file information, the instance of the object itself must be stored in a bind context by using the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a> method with the <i>pszKey</i> parameter set to <code>L"File System Bind Data"</code>.