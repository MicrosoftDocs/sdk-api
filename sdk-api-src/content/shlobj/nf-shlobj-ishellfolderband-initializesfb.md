---
UID: NF:shlobj.IShellFolderBand.InitializeSFB
title: IShellFolderBand::InitializeSFB (shlobj.h)
description: Initializes an IShellFolderBand object.
helpviewer_keywords: ["IShellFolderBand interface [Windows Shell]","InitializeSFB method","IShellFolderBand.InitializeSFB","IShellFolderBand::InitializeSFB","InitializeSFB","InitializeSFB method [Windows Shell]","InitializeSFB method [Windows Shell]","IShellFolderBand interface","_win32_IShellFolderBand_InitializeSFB","shell.IShellFolderBand_InitializeSFB","shlobj/IShellFolderBand::InitializeSFB"]
old-location: shell\IShellFolderBand_InitializeSFB.htm
tech.root: shell
ms.assetid: 2f0582d2-b079-4b97-8da0-211b6ef1b8f3
ms.date: 12/05/2018
ms.keywords: IShellFolderBand interface [Windows Shell],InitializeSFB method, IShellFolderBand.InitializeSFB, IShellFolderBand::InitializeSFB, InitializeSFB, InitializeSFB method [Windows Shell], InitializeSFB method [Windows Shell],IShellFolderBand interface, _win32_IShellFolderBand_InitializeSFB, shell.IShellFolderBand_InitializeSFB, shlobj/IShellFolderBand::InitializeSFB
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shlobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderBand::InitializeSFB
 - shlobj/IShellFolderBand::InitializeSFB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolderBand.InitializeSFB
---

# IShellFolderBand::InitializeSFB


## -description

Initializes an <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband">IShellFolderBand</a> object.

## -parameters

### -param psf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object.

### -param pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband">IShellFolderBand</a>