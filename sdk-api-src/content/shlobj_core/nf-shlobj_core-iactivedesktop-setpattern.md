---
UID: NF:shlobj_core.IActiveDesktop.SetPattern
title: IActiveDesktop::SetPattern (shlobj_core.h)
description: Sets the Active Desktop pattern.
helpviewer_keywords: ["IActiveDesktop interface [Legacy Windows Environment Features]","SetPattern method","IActiveDesktop.SetPattern","IActiveDesktop::SetPattern","SetPattern","SetPattern method [Legacy Windows Environment Features]","SetPattern method [Legacy Windows Environment Features]","IActiveDesktop interface","_win32_IActiveDesktop_SetPattern","lwef.iactivedesktop_setpattern","shell.iactivedesktop_setpattern","shlobj_core/IActiveDesktop::SetPattern"]
old-location: lwef\iactivedesktop_setpattern.htm
tech.root: lwef
ms.assetid: ca66a200-dd12-454b-b449-feeae26941b6
ms.date: 12/05/2018
ms.keywords: IActiveDesktop interface [Legacy Windows Environment Features],SetPattern method, IActiveDesktop.SetPattern, IActiveDesktop::SetPattern, SetPattern, SetPattern method [Legacy Windows Environment Features], SetPattern method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_SetPattern, lwef.iactivedesktop_setpattern, shell.iactivedesktop_setpattern, shlobj_core/IActiveDesktop::SetPattern
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
 - IActiveDesktop::SetPattern
 - shlobj_core/IActiveDesktop::SetPattern
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
 - IActiveDesktop.SetPattern
---

# IActiveDesktop::SetPattern


## -description

Sets the Active Desktop pattern.

## -parameters

### -param pwszPattern [in]

Type: <b>PCWSTR</b>

The address of a string value that contains a string of decimals whose bit pattern represents a picture. Each decimal represents the on/off state of the 8 pixels in that row.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>