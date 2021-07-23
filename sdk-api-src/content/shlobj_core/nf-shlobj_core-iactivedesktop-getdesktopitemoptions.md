---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItemOptions
title: IActiveDesktop::GetDesktopItemOptions (shlobj_core.h)
description: Gets the options for the desktop item.
helpviewer_keywords: ["GetDesktopItemOptions","GetDesktopItemOptions method [Legacy Windows Environment Features]","GetDesktopItemOptions method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetDesktopItemOptions method","IActiveDesktop.GetDesktopItemOptions","IActiveDesktop::GetDesktopItemOptions","_win32_IActiveDesktop_GetDesktopItemOptions","lwef.iactivedesktop_getdesktopitemoptions","shell.iactivedesktop_getdesktopitemoptions","shlobj_core/IActiveDesktop::GetDesktopItemOptions"]
old-location: lwef\iactivedesktop_getdesktopitemoptions.htm
tech.root: lwef
ms.assetid: 3717b67a-b028-44a9-af1c-a6a94b2d76d8
ms.date: 12/05/2018
ms.keywords: GetDesktopItemOptions, GetDesktopItemOptions method [Legacy Windows Environment Features], GetDesktopItemOptions method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItemOptions method, IActiveDesktop.GetDesktopItemOptions, IActiveDesktop::GetDesktopItemOptions, _win32_IActiveDesktop_GetDesktopItemOptions, lwef.iactivedesktop_getdesktopitemoptions, shell.iactivedesktop_getdesktopitemoptions, shlobj_core/IActiveDesktop::GetDesktopItemOptions
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
 - IActiveDesktop::GetDesktopItemOptions
 - shlobj_core/IActiveDesktop::GetDesktopItemOptions
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
 - IActiveDesktop.GetDesktopItemOptions
---

# IActiveDesktop::GetDesktopItemOptions


## -description

Gets the options for the desktop item.

## -parameters

### -param pco [in, out]

Type: <b>LPCOMPONENTSOPT</b>

The address of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-componentsopt">COMPONENTSOPT</a> structure containing the options that are currently set.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>