---
UID: NF:shlobj_core.IActiveDesktop.RemoveDesktopItem
title: IActiveDesktop::RemoveDesktopItem (shlobj_core.h)
description: Removes the specified desktop item from the desktop.
helpviewer_keywords: ["IActiveDesktop interface [Legacy Windows Environment Features]","RemoveDesktopItem method","IActiveDesktop.RemoveDesktopItem","IActiveDesktop::RemoveDesktopItem","RemoveDesktopItem","RemoveDesktopItem method [Legacy Windows Environment Features]","RemoveDesktopItem method [Legacy Windows Environment Features]","IActiveDesktop interface","_win32_IActiveDesktop_RemoveDesktopItem","lwef.iactivedesktop_removedesktopitem","shell.iactivedesktop_removedesktopitem","shlobj_core/IActiveDesktop::RemoveDesktopItem"]
old-location: lwef\iactivedesktop_removedesktopitem.htm
tech.root: lwef
ms.assetid: 6fee6c97-0605-4ad3-90fb-c5271f78536a
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],RemoveDesktopItem method, IActiveDesktop.RemoveDesktopItem, IActiveDesktop::RemoveDesktopItem, RemoveDesktopItem, RemoveDesktopItem method [Legacy Windows Environment Features], RemoveDesktopItem method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_RemoveDesktopItem, lwef.iactivedesktop_removedesktopitem, shell.iactivedesktop_removedesktopitem, shlobj_core/IActiveDesktop::RemoveDesktopItem
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
 - IActiveDesktop::RemoveDesktopItem
 - shlobj_core/IActiveDesktop::RemoveDesktopItem
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
 - IActiveDesktop.RemoveDesktopItem
---

# IActiveDesktop::RemoveDesktopItem


## -description

Removes the specified desktop item from the desktop.

## -parameters

### -param pcomp [in]

Type: <b>LPCCOMPONENT</b>

The address of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure that specifies the item to be removed. The desktop item associated with the <b>wszSource</b> member of the structure will be removed.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>