---
UID: NF:shldisp.IShellFolderViewDual3.get_FolderFlags
title: IShellFolderViewDual3::get_FolderFlags (shldisp.h)
description: Gets the settings for the current folder.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","get_FolderFlags method","IShellFolderViewDual3.get_FolderFlags","IShellFolderViewDual3::get_FolderFlags","_shell_IShellFolderViewDual3_get_FolderFlags","get_FolderFlags","get_FolderFlags method [Windows Shell]","get_FolderFlags method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_get_FolderFlags","shldisp/IShellFolderViewDual3::get_FolderFlags"]
old-location: shell\IShellFolderViewDual3_get_FolderFlags.htm
tech.root: shell
ms.assetid: c0fc82d4-d27e-4410-88a8-83839de8409b
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_FolderFlags method, IShellFolderViewDual3.get_FolderFlags, IShellFolderViewDual3::get_FolderFlags, _shell_IShellFolderViewDual3_get_FolderFlags, get_FolderFlags, get_FolderFlags method [Windows Shell], get_FolderFlags method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_FolderFlags, shldisp/IShellFolderViewDual3::get_FolderFlags
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - IShellFolderViewDual3::get_FolderFlags
 - shldisp/IShellFolderViewDual3::get_FolderFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual3.get_FolderFlags
---

# IShellFolderViewDual3::get_FolderFlags


## -description

Gets the settings for the current folder.

## -parameters

### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the current setting flags.  For a list of possible values, see <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.