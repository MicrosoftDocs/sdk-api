---
UID: NF:shlobj_core.IActiveDesktop.GetPattern
title: IActiveDesktop::GetPattern (shlobj_core.h)
description: Gets the current pattern.
helpviewer_keywords: ["GetPattern","GetPattern method [Legacy Windows Environment Features]","GetPattern method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","GetPattern method","IActiveDesktop.GetPattern","IActiveDesktop::GetPattern","_win32_IActiveDesktop_GetPattern","lwef.iactivedesktop_getpattern","shell.iactivedesktop_getpattern","shlobj_core/IActiveDesktop::GetPattern"]
old-location: lwef\iactivedesktop_getpattern.htm
tech.root: lwef
ms.assetid: e4211868-9f06-412c-b0b5-ba6ce395708e
ms.date: 12/05/2018
ms.keywords: GetPattern, GetPattern method [Legacy Windows Environment Features], GetPattern method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],GetPattern method, IActiveDesktop.GetPattern, IActiveDesktop::GetPattern, _win32_IActiveDesktop_GetPattern, lwef.iactivedesktop_getpattern, shell.iactivedesktop_getpattern, shlobj_core/IActiveDesktop::GetPattern
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
 - IActiveDesktop::GetPattern
 - shlobj_core/IActiveDesktop::GetPattern
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
 - IActiveDesktop.GetPattern
---

# IActiveDesktop::GetPattern


## -description

Gets the current pattern.

## -parameters

### -param pwszPattern [out]

Type: <b>PWSTR</b>

A pointer to a null-terminated, Unicode buffer containing a string of decimals whose bit pattern represents a picture. Each decimal represents the on/off state of the 8 pixels in that row.

### -param cchPattern

Type: <b>UINT</b>

The size of the <i>pwszPattern</i> string, in characters.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

