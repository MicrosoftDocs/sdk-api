---
UID: NF:shlobj.IShellFolderBand.SetBandInfoSFB
title: IShellFolderBand::SetBandInfoSFB (shlobj.h)
description: Uses the information in a BANDINFOSFB structure to set the band information for a IShellFolderBand object.
helpviewer_keywords: ["IShellFolderBand interface [Windows Shell]","SetBandInfoSFB method","IShellFolderBand.SetBandInfoSFB","IShellFolderBand::SetBandInfoSFB","SetBandInfoSFB","SetBandInfoSFB method [Windows Shell]","SetBandInfoSFB method [Windows Shell]","IShellFolderBand interface","_win32_IShellFolderBand_SetBandInfoSFB","shell.IShellFolderBand_SetBandInfoSFB","shlobj/IShellFolderBand::SetBandInfoSFB"]
old-location: shell\IShellFolderBand_SetBandInfoSFB.htm
tech.root: shell
ms.assetid: 6b1a219f-60a3-4073-8293-2e9e1c6459d9
ms.date: 12/05/2018
ms.keywords: IShellFolderBand interface [Windows Shell],SetBandInfoSFB method, IShellFolderBand.SetBandInfoSFB, IShellFolderBand::SetBandInfoSFB, SetBandInfoSFB, SetBandInfoSFB method [Windows Shell], SetBandInfoSFB method [Windows Shell],IShellFolderBand interface, _win32_IShellFolderBand_SetBandInfoSFB, shell.IShellFolderBand_SetBandInfoSFB, shlobj/IShellFolderBand::SetBandInfoSFB
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
 - IShellFolderBand::SetBandInfoSFB
 - shlobj/IShellFolderBand::SetBandInfoSFB
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
 - IShellFolderBand.SetBandInfoSFB
---

# IShellFolderBand::SetBandInfoSFB


## -description

Uses the information in a <a href="/windows/desktop/api/shlobj/ns-shlobj-bandinfosfb">BANDINFOSFB</a> structure to set the band information for a <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband">IShellFolderBand</a> object.

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