---
UID: NF:shobjidl_core.IFolderView2.SetCurrentFolderFlags
title: IFolderView2::SetCurrentFolderFlags (shobjidl_core.h)
description: Sets and applies specified folder flags.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetCurrentFolderFlags method","IFolderView2.SetCurrentFolderFlags","IFolderView2::SetCurrentFolderFlags","SetCurrentFolderFlags","SetCurrentFolderFlags method [Windows Shell]","SetCurrentFolderFlags method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetCurrentFolderFlags","shell.IFolderView2_SetCurrentFolderFlags","shobjidl_core/IFolderView2::SetCurrentFolderFlags"]
old-location: shell\IFolderView2_SetCurrentFolderFlags.htm
tech.root: shell
ms.assetid: 94999ac7-c9dd-439e-8f63-eeb226763200
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetCurrentFolderFlags method, IFolderView2.SetCurrentFolderFlags, IFolderView2::SetCurrentFolderFlags, SetCurrentFolderFlags, SetCurrentFolderFlags method [Windows Shell], SetCurrentFolderFlags method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetCurrentFolderFlags, shell.IFolderView2_SetCurrentFolderFlags, shobjidl_core/IFolderView2::SetCurrentFolderFlags
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IFolderView2::SetCurrentFolderFlags
 - shobjidl_core/IFolderView2::SetCurrentFolderFlags
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
 - IFolderView2.SetCurrentFolderFlags
---

# IFolderView2::SetCurrentFolderFlags


## -description

Sets and applies specified folder flags.

## -parameters

### -param dwMask [in]

Type: <b>DWORD</b>

The value of type <b>DWORD</b> that specifies the bitmask indicating which items in the structure are desired or valid.

### -param dwFlags [in]

Type: <b>DWORD</b>

The value of type <b>DWORD</b> that contains one or more <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags">FOLDERFLAGS</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>For Windows 7 or later:</b> This method must be used in combination with the <i>FVO_CUSTOMPOSITION</i> flag from the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a> enumeration.