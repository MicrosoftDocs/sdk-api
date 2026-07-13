---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItemCount
title: IActiveDesktop::GetDesktopItemCount (shlobj_core.h)
description: Gets a count of the desktop items.
helpviewer_keywords: ["GetDesktopItemCount","GetDesktopItemCount method [Legacy Windows Environment Features]","GetDesktopItemCount method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetDesktopItemCount method","IActiveDesktop.GetDesktopItemCount","IActiveDesktop::GetDesktopItemCount","_win32_IActiveDesktop_GetDesktopItemCount","lwef.iactivedesktop_getdesktopitemcount","shell.iactivedesktop_getdesktopitemcount","shlobj_core/IActiveDesktop::GetDesktopItemCount"]
old-location: lwef\iactivedesktop_getdesktopitemcount.htm
tech.root: lwef
ms.assetid: d2bba6f8-4ff0-4978-93ae-46db9ec6ea48
ms.date: 12/05/2018
ms.keywords: GetDesktopItemCount, GetDesktopItemCount method [Legacy Windows Environment Features], GetDesktopItemCount method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItemCount method, IActiveDesktop.GetDesktopItemCount, IActiveDesktop::GetDesktopItemCount, _win32_IActiveDesktop_GetDesktopItemCount, lwef.iactivedesktop_getdesktopitemcount, shell.iactivedesktop_getdesktopitemcount, shlobj_core/IActiveDesktop::GetDesktopItemCount
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
 - IActiveDesktop::GetDesktopItemCount
 - shlobj_core/IActiveDesktop::GetDesktopItemCount
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
 - IActiveDesktop.GetDesktopItemCount
---

# IActiveDesktop::GetDesktopItemCount


## -description

Gets a count of the desktop items.

## -parameters

### -param pcItems [out]

Type: <b>int*</b>

A pointer to an <b>int</b> value that, when this method returns successfully, contains the count.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value pointed to by <i>pcItems</i> can be used to enumerate all desktop items. Desktop items have index values which start at zero and go to one less than the value pointed to by <i>pcItems</i>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>