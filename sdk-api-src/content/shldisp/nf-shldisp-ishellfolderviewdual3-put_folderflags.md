---
UID: NF:shldisp.IShellFolderViewDual3.put_FolderFlags
title: IShellFolderViewDual3::put_FolderFlags (shldisp.h)
description: Sets the current folders settings.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","put_FolderFlags method","IShellFolderViewDual3.put_FolderFlags","IShellFolderViewDual3::put_FolderFlags","_shell_IShellFolderViewDual3_put_FolderFlags","put_FolderFlags","put_FolderFlags method [Windows Shell]","put_FolderFlags method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_put_FolderFlags","shldisp/IShellFolderViewDual3::put_FolderFlags"]
old-location: shell\IShellFolderViewDual3_put_FolderFlags.htm
tech.root: shell
ms.assetid: 698678a6-3624-420a-997a-9fd1e61d67e6
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],put_FolderFlags method, IShellFolderViewDual3.put_FolderFlags, IShellFolderViewDual3::put_FolderFlags, _shell_IShellFolderViewDual3_put_FolderFlags, put_FolderFlags, put_FolderFlags method [Windows Shell], put_FolderFlags method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_put_FolderFlags, shldisp/IShellFolderViewDual3::put_FolderFlags
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
 - IShellFolderViewDual3::put_FolderFlags
 - shldisp/IShellFolderViewDual3::put_FolderFlags
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
 - IShellFolderViewDual3.put_FolderFlags
---

# IShellFolderViewDual3::put_FolderFlags


## -description

Sets the current folders settings.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that determine the folder settings. For a list of possible values, see <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.