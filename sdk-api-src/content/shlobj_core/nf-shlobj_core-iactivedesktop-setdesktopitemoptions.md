---
UID: NF:shlobj_core.IActiveDesktop.SetDesktopItemOptions
title: IActiveDesktop::SetDesktopItemOptions (shlobj_core.h)
description: Sets the item's options.
helpviewer_keywords: ["IActiveDesktop interface [Legacy Windows Environment Features]","SetDesktopItemOptions method","IActiveDesktop.SetDesktopItemOptions","IActiveDesktop::SetDesktopItemOptions","SetDesktopItemOptions","SetDesktopItemOptions method [Legacy Windows Environment Features]","SetDesktopItemOptions method [Legacy Windows Environment Features]","IActiveDesktop interface","_win32_IActiveDesktop_SetDesktopItemOptions","lwef.iactivedesktop_setdesktopitemoptions","shell.iactivedesktop_setdesktopitemoptions","shlobj_core/IActiveDesktop::SetDesktopItemOptions"]
old-location: lwef\iactivedesktop_setdesktopitemoptions.htm
tech.root: lwef
ms.assetid: 5f2c1f41-d678-4eb8-b246-46133eec465f
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetDesktopItemOptions method, IActiveDesktop.SetDesktopItemOptions, IActiveDesktop::SetDesktopItemOptions, SetDesktopItemOptions, SetDesktopItemOptions method [Legacy Windows Environment Features], SetDesktopItemOptions method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetDesktopItemOptions, lwef.iactivedesktop_setdesktopitemoptions, shell.iactivedesktop_setdesktopitemoptions, shlobj_core/IActiveDesktop::SetDesktopItemOptions
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop::SetDesktopItemOptions
 - shlobj_core/IActiveDesktop::SetDesktopItemOptions
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
 - IActiveDesktop.SetDesktopItemOptions
---

# IActiveDesktop::SetDesktopItemOptions


## -description

Sets the item's options.

## -parameters

### -param pco [in]

Type: <b>LPCCOMPONENTSOPT</b>

The address of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-componentsopt">COMPONENTSOPT</a> structure that contains the options to set.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>