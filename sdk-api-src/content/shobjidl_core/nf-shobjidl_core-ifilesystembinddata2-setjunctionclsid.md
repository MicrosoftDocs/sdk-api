---
UID: NF:shobjidl_core.IFileSystemBindData2.SetJunctionCLSID
title: IFileSystemBindData2::SetJunctionCLSID (shobjidl_core.h)
description: Sets the class identifier (CLSID) of the object that implements IShellFolder, if the current item is a junction point.
helpviewer_keywords: ["IFileSystemBindData2 interface [Windows Shell]","SetJunctionCLSID method","IFileSystemBindData2.SetJunctionCLSID","IFileSystemBindData2::SetJunctionCLSID","SetJunctionCLSID","SetJunctionCLSID method [Windows Shell]","SetJunctionCLSID method [Windows Shell]","IFileSystemBindData2 interface","_shell_IFileSystemBindData2_SetJunctionCLSID","shell.IFileSystemBindData2_SetJunctionCLSID","shobjidl_core/IFileSystemBindData2::SetJunctionCLSID"]
old-location: shell\IFileSystemBindData2_SetJunctionCLSID.htm
tech.root: shell
ms.assetid: e072818d-dfa4-4b95-93b6-275206596147
ms.date: 12/05/2018
ms.keywords: IFileSystemBindData2 interface [Windows Shell],SetJunctionCLSID method, IFileSystemBindData2.SetJunctionCLSID, IFileSystemBindData2::SetJunctionCLSID, SetJunctionCLSID, SetJunctionCLSID method [Windows Shell], SetJunctionCLSID method [Windows Shell],IFileSystemBindData2 interface, _shell_IFileSystemBindData2_SetJunctionCLSID, shell.IFileSystemBindData2_SetJunctionCLSID, shobjidl_core/IFileSystemBindData2::SetJunctionCLSID
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
 - IFileSystemBindData2::SetJunctionCLSID
 - shobjidl_core/IFileSystemBindData2::SetJunctionCLSID
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
 - IFileSystemBindData2.SetJunctionCLSID
---

# IFileSystemBindData2::SetJunctionCLSID


## -description

Sets the class identifier (CLSID) of the object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>, if the current item is a junction point.

## -parameters

### -param clsid [in]

Type: <b>REFCLSID</b>

The CLSID for the object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> with a junction point as its current item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.