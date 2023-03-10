---
UID: NF:winuser.GetKBCodePage
title: GetKBCodePage function (winuser.h)
description: Retrieves the current code page.
helpviewer_keywords: ["GetKBCodePage","GetKBCodePage function [Keyboard and Mouse Input]","_win32_GetKBCodePage","_win32_getkbcodepage_cpp","inputdev.getkbcodepage","winui._win32_getkbcodepage","winuser/GetKBCodePage"]
old-location: inputdev\getkbcodepage.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkbcodepage.htm
ms.date: 12/05/2018
ms.keywords: GetKBCodePage, GetKBCodePage function [Keyboard and Mouse Input], _win32_GetKBCodePage, _win32_getkbcodepage_cpp, inputdev.getkbcodepage, winui._win32_getkbcodepage, winuser/GetKBCodePage
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetKBCodePage
 - winuser/GetKBCodePage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetKBCodePage
---

# GetKBCodePage function


## -description

Retrieves the current code page.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a> function to retrieve the OEM code-page identifier for the system.</div><div> </div>



## -returns

Type: <b>UINT</b>

The return value is an OEM code-page identifier, or it is the default identifier if the registry value is not readable. For a list of OEM code-page identifiers, see <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winnls/nf-winnls-getacp">GetACP</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>
