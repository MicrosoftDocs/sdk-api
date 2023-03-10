---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItemBySource
title: IActiveDesktop::GetDesktopItemBySource (shlobj_core.h)
description: Gets a desktop item using its source URL.
helpviewer_keywords: ["GetDesktopItemBySource","GetDesktopItemBySource method [Legacy Windows Environment Features]","GetDesktopItemBySource method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetDesktopItemBySource method","IActiveDesktop.GetDesktopItemBySource","IActiveDesktop::GetDesktopItemBySource","_win32_IActiveDesktop_GetDesktopItemBySource","lwef.iactivedesktop_getdesktopitembysource","shell.iactivedesktop_getdesktopitembysource","shlobj_core/IActiveDesktop::GetDesktopItemBySource"]
old-location: lwef\iactivedesktop_getdesktopitembysource.htm
tech.root: lwef
ms.assetid: 9449238a-c1af-493c-9c23-503317fe6656
ms.date: 12/05/2018
ms.keywords: GetDesktopItemBySource, GetDesktopItemBySource method [Legacy Windows Environment Features], GetDesktopItemBySource method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItemBySource method, IActiveDesktop.GetDesktopItemBySource, IActiveDesktop::GetDesktopItemBySource, _win32_IActiveDesktop_GetDesktopItemBySource, lwef.iactivedesktop_getdesktopitembysource, shell.iactivedesktop_getdesktopitembysource, shlobj_core/IActiveDesktop::GetDesktopItemBySource
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
 - IActiveDesktop::GetDesktopItemBySource
 - shlobj_core/IActiveDesktop::GetDesktopItemBySource
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
 - IActiveDesktop.GetDesktopItemBySource
---

# IActiveDesktop::GetDesktopItemBySource


## -description

Gets a desktop item using its source URL.

## -parameters

### -param pwszSource [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the source URL of the desktop item.

### -param pcomp [in, out]

Type: <b>LPCOMPONENT</b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure that, when this method returns successfully, receives the details about the desktop item. On entry, the size of the structure must be set.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>