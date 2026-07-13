---
UID: NF:shobjidl_core.IFileSystemBindData2.GetJunctionCLSID
title: IFileSystemBindData2::GetJunctionCLSID (shobjidl_core.h)
description: Gets the class identifier (CLSID) of the object that implements IShellFolder for the item, if the item is a junction point.
helpviewer_keywords: ["GetJunctionCLSID","GetJunctionCLSID method [Windows Shell]","GetJunctionCLSID method [Windows Shell]","IFileSystemBindData2 interface","IFileSystemBindData2 interface [Windows Shell]","GetJunctionCLSID method","IFileSystemBindData2.GetJunctionCLSID","IFileSystemBindData2::GetJunctionCLSID","_shell_IFileSystemBindData2_GetJunctionCLSID","shell.IFileSystemBindData2_GetJunctionCLSID","shobjidl_core/IFileSystemBindData2::GetJunctionCLSID"]
old-location: shell\IFileSystemBindData2_GetJunctionCLSID.htm
tech.root: shell
ms.assetid: 57c5205a-9a56-4c47-bec4-11a690107bc6
ms.date: 12/05/2018
ms.keywords: GetJunctionCLSID, GetJunctionCLSID method [Windows Shell], GetJunctionCLSID method [Windows Shell],IFileSystemBindData2 interface, IFileSystemBindData2 interface [Windows Shell],GetJunctionCLSID method, IFileSystemBindData2.GetJunctionCLSID, IFileSystemBindData2::GetJunctionCLSID, _shell_IFileSystemBindData2_GetJunctionCLSID, shell.IFileSystemBindData2_GetJunctionCLSID, shobjidl_core/IFileSystemBindData2::GetJunctionCLSID
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
 - IFileSystemBindData2::GetJunctionCLSID
 - shobjidl_core/IFileSystemBindData2::GetJunctionCLSID
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
 - IFileSystemBindData2.GetJunctionCLSID
---

# IFileSystemBindData2::GetJunctionCLSID


## -description

Gets the class identifier (CLSID) of the object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> for the item, if the item is a junction point.

## -parameters

### -param pclsid [out]

Type: <b>CLSID*</b>

When this method returns successfully, receives a pointer to the CLSID of the object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> for the current item, if the item is a junction point.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.