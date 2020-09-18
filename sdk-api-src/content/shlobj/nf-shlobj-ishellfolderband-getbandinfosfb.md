---
UID: NF:shlobj.IShellFolderBand.GetBandInfoSFB
title: IShellFolderBand::GetBandInfoSFB (shlobj.h)
description: Gets information concerning an IShellFolderBand object and places it in a BANDINFOSFB structure.
helpviewer_keywords: ["GetBandInfoSFB","GetBandInfoSFB method [Windows Shell]","GetBandInfoSFB method [Windows Shell]","IShellFolderBand interface","IShellFolderBand interface [Windows Shell]","GetBandInfoSFB method","IShellFolderBand.GetBandInfoSFB","IShellFolderBand::GetBandInfoSFB","_win32_IShellFolderBand_GetBandInfoSFB","shell.IShellFolderBand_GetBandInfoSFB","shlobj/IShellFolderBand::GetBandInfoSFB"]
old-location: shell\IShellFolderBand_GetBandInfoSFB.htm
tech.root: shell
ms.assetid: 7a42ba12-987a-4b43-9d95-085a5e896245
ms.date: 12/05/2018
ms.keywords: GetBandInfoSFB, GetBandInfoSFB method [Windows Shell], GetBandInfoSFB method [Windows Shell],IShellFolderBand interface, IShellFolderBand interface [Windows Shell],GetBandInfoSFB method, IShellFolderBand.GetBandInfoSFB, IShellFolderBand::GetBandInfoSFB, _win32_IShellFolderBand_GetBandInfoSFB, shell.IShellFolderBand_GetBandInfoSFB, shlobj/IShellFolderBand::GetBandInfoSFB
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderBand::GetBandInfoSFB
 - shlobj/IShellFolderBand::GetBandInfoSFB
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
 - IShellFolderBand.GetBandInfoSFB
---

# IShellFolderBand::GetBandInfoSFB


## -description

Gets information concerning an <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband">IShellFolderBand</a> object and places it in a <a href="/windows/desktop/api/shlobj/ns-shlobj-bandinfosfb">BANDINFOSFB</a> structure.

## -parameters

### -param pbi

Type: <b>PBANDINFOSFB</b>

A pointer to a <a href="/windows/desktop/api/shlobj/ns-shlobj-bandinfosfb">BANDINFOSFB</a> structure.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband">IShellFolderBand</a>