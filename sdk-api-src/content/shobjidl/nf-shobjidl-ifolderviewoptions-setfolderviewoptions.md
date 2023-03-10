---
UID: NF:shobjidl.IFolderViewOptions.SetFolderViewOptions
title: IFolderViewOptions::SetFolderViewOptions (shobjidl.h)
description: Sets specified options for the view.
helpviewer_keywords: ["IFolderViewOptions interface [Windows Shell]","SetFolderViewOptions method","IFolderViewOptions.SetFolderViewOptions","IFolderViewOptions::SetFolderViewOptions","SetFolderViewOptions","SetFolderViewOptions method [Windows Shell]","SetFolderViewOptions method [Windows Shell]","IFolderViewOptions interface","_shell_IFolderViewOptions_SetFolderViewOptions","shell.IFolderViewOptions_SetFolderViewOptions","shobjidl/IFolderViewOptions::SetFolderViewOptions"]
old-location: shell\IFolderViewOptions_SetFolderViewOptions.htm
tech.root: shell
ms.assetid: e170f60f-9b6c-4765-8aad-b370b08db053
ms.date: 12/05/2018
ms.keywords: IFolderViewOptions interface [Windows Shell],SetFolderViewOptions method, IFolderViewOptions.SetFolderViewOptions, IFolderViewOptions::SetFolderViewOptions, SetFolderViewOptions, SetFolderViewOptions method [Windows Shell], SetFolderViewOptions method [Windows Shell],IFolderViewOptions interface, _shell_IFolderViewOptions_SetFolderViewOptions, shell.IFolderViewOptions_SetFolderViewOptions, shobjidl/IFolderViewOptions::SetFolderViewOptions
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.dll: ExplorerFrame.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderViewOptions::SetFolderViewOptions
 - shobjidl/IFolderViewOptions::SetFolderViewOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ExplorerFrame.dll
api_name:
 - IFolderViewOptions.SetFolderViewOptions
---

# IFolderViewOptions::SetFolderViewOptions


## -description

Sets specified options for the view.

## -parameters

### -param fvoMask [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a></b>

A bitmask made up of one or more of the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a> flags to indicate which options' are being changed. Values in <i>fvoFlags</i> not included in this mask are ignored.

### -param fvoFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a></b>

A bitmask that contains the new values for the options specified in <i>fvoMask</i>. To enable an option, the bitmask should include the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a> flag for that option. To disable an option, the bit used for that <b>FOLDERVIEWOPTIONS</b> flag should be 0.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.