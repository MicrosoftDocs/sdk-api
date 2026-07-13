---
UID: NF:shlobj_core.IActiveDesktop.GetDesktopItemByID
title: IActiveDesktop::GetDesktopItemByID (shlobj_core.h)
description: Gets the desktop item that matches the given identification.
helpviewer_keywords: ["GetDesktopItemByID","GetDesktopItemByID method [Legacy Windows Environment Features]","GetDesktopItemByID method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetDesktopItemByID method","IActiveDesktop.GetDesktopItemByID","IActiveDesktop::GetDesktopItemByID","_win32_IActiveDesktop_GetDesktopItemByID","lwef.iactivedesktop_getdesktopitembyid","shell.iactivedesktop_getdesktopitembyid","shlobj_core/IActiveDesktop::GetDesktopItemByID"]
old-location: lwef\iactivedesktop_getdesktopitembyid.htm
tech.root: lwef
ms.assetid: 44e5fc48-b50d-4410-87c8-7e42634218bf
ms.date: 12/05/2018
ms.keywords: GetDesktopItemByID, GetDesktopItemByID method [Legacy Windows Environment Features], GetDesktopItemByID method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetDesktopItemByID method, IActiveDesktop.GetDesktopItemByID, IActiveDesktop::GetDesktopItemByID, _win32_IActiveDesktop_GetDesktopItemByID, lwef.iactivedesktop_getdesktopitembyid, shell.iactivedesktop_getdesktopitembyid, shlobj_core/IActiveDesktop::GetDesktopItemByID
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
 - IActiveDesktop::GetDesktopItemByID
 - shlobj_core/IActiveDesktop::GetDesktopItemByID
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
 - IActiveDesktop.GetDesktopItemByID
---

# IActiveDesktop::GetDesktopItemByID


## -description

Gets the desktop item that matches the given identification.

## -parameters

### -param dwID

Type: <b>ULONG_PTR</b>

An unsigned long integer value that contains the desktop item's identification.

### -param pcomp [in, out]

Type: <b>LPCOMPONENT</b>

The address of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure of the retrieved desktop item.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The desktop item's identification is returned in the <b>dwID</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure that is returned from the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem">IActiveDesktop::GetDesktopItem</a> method. This identification is only valid until the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges">IActiveDesktop::ApplyChanges</a> method is called. Applications that must retrieve the same desktop item consistently should enumerate the desktop items using the <b>IActiveDesktop::GetDesktopItem</b> and <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount">IActiveDesktop::GetDesktopItemCount</a> methods.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>