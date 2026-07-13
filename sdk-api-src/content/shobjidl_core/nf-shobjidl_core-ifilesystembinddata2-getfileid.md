---
UID: NF:shobjidl_core.IFileSystemBindData2.GetFileID
title: IFileSystemBindData2::GetFileID (shobjidl_core.h)
description: Gets the unique file identifier for the current file.
helpviewer_keywords: ["GetFileID","GetFileID method [Windows Shell]","GetFileID method [Windows Shell]","IFileSystemBindData2 interface","IFileSystemBindData2 interface [Windows Shell]","GetFileID method","IFileSystemBindData2.GetFileID","IFileSystemBindData2::GetFileID","_shell_IFileSystemBindData2_GetFileID","shell.IFileSystemBindData2_GetFileID","shobjidl_core/IFileSystemBindData2::GetFileID"]
old-location: shell\IFileSystemBindData2_GetFileID.htm
tech.root: shell
ms.assetid: 77052ae5-d663-4bf8-967a-29bd5dc85706
ms.date: 12/05/2018
ms.keywords: GetFileID, GetFileID method [Windows Shell], GetFileID method [Windows Shell],IFileSystemBindData2 interface, IFileSystemBindData2 interface [Windows Shell],GetFileID method, IFileSystemBindData2.GetFileID, IFileSystemBindData2::GetFileID, _shell_IFileSystemBindData2_GetFileID, shell.IFileSystemBindData2_GetFileID, shobjidl_core/IFileSystemBindData2::GetFileID
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemBindData2::GetFileID
 - shobjidl_core/IFileSystemBindData2::GetFileID
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
 - IFileSystemBindData2.GetFileID
---

# IFileSystemBindData2::GetFileID


## -description

Gets the unique file identifier for the current file.

## -parameters

### -param pliFileID [out]

Type: <b>LARGE_INTEGER*</b>

When this method returns successfully, receives a pointer to the unique file identifier for the current file. <i>pliFileID</i> is a pointer to a value that is a concatenation of the values <i>nFileIndexHigh</i> and <i>nFileIndexlow</i>, noted in structure <a href="/windows/desktop/api/fileapi/ns-fileapi-by_handle_file_information">_by_handle_file_information</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.