---
UID: NF:shobjidl.IFolderViewOptions.GetFolderViewOptions
title: IFolderViewOptions::GetFolderViewOptions (shobjidl.h)
description: Retrieves the current set of options for the view.
helpviewer_keywords: ["GetFolderViewOptions","GetFolderViewOptions method [Windows Shell]","GetFolderViewOptions method [Windows Shell]","IFolderViewOptions interface","IFolderViewOptions interface [Windows Shell]","GetFolderViewOptions method","IFolderViewOptions.GetFolderViewOptions","IFolderViewOptions::GetFolderViewOptions","_shell_IFolderViewOptions_GetFolderViewOptions","shell.IFolderViewOptions_GetFolderViewOptions","shobjidl/IFolderViewOptions::GetFolderViewOptions"]
old-location: shell\IFolderViewOptions_GetFolderViewOptions.htm
tech.root: shell
ms.assetid: 9733c2b0-608f-4f20-b379-81de0c333473
ms.date: 12/05/2018
ms.keywords: GetFolderViewOptions, GetFolderViewOptions method [Windows Shell], GetFolderViewOptions method [Windows Shell],IFolderViewOptions interface, IFolderViewOptions interface [Windows Shell],GetFolderViewOptions method, IFolderViewOptions.GetFolderViewOptions, IFolderViewOptions::GetFolderViewOptions, _shell_IFolderViewOptions_GetFolderViewOptions, shell.IFolderViewOptions_GetFolderViewOptions, shobjidl/IFolderViewOptions::GetFolderViewOptions
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
 - IFolderViewOptions::GetFolderViewOptions
 - shobjidl/IFolderViewOptions::GetFolderViewOptions
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
 - IFolderViewOptions.GetFolderViewOptions
---

# IFolderViewOptions::GetFolderViewOptions


## -description

Retrieves the current set of options for the view.

## -parameters

### -param pfvoFlags [out]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a>*</b>

A bitmask that, when this method returns successfully, receives the <a href="/windows/desktop/api/shobjidl/ne-shobjidl-folderviewoptions">FOLDERVIEWOPTIONS</a> values that are currently set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.