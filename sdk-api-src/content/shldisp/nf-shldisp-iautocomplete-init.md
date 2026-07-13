---
UID: NF:shldisp.IAutoComplete.Init
title: IAutoComplete::Init (shldisp.h)
description: Initializes the autocomplete object.
helpviewer_keywords: ["IAutoComplete interface [Windows Shell]","Init method","IAutoComplete.Init","IAutoComplete::Init","Init","Init method [Windows Shell]","Init method [Windows Shell]","IAutoComplete interface","_win32_IAutoComplete_Init","shell.IAutoComplete_Init","shldisp/IAutoComplete::Init"]
old-location: shell\IAutoComplete_Init.htm
tech.root: shell
ms.assetid: e5ee36b7-11b4-4eca-ae8e-eefa6245f287
ms.date: 12/05/2018
ms.keywords: IAutoComplete interface [Windows Shell],Init method, IAutoComplete.Init, IAutoComplete::Init, Init, Init method [Windows Shell], Init method [Windows Shell],IAutoComplete interface, _win32_IAutoComplete_Init, shell.IAutoComplete_Init, shldisp/IAutoComplete::Init
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutoComplete::Init
 - shldisp/IAutoComplete::Init
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
 - IAutoComplete.Init
---

# IAutoComplete::Init


## -description

Initializes the autocomplete object.

## -parameters

### -param hwndEdit [in]

Type: <b>HWND</b>

A handle to the window for the system edit control for which autocompletion will be enabled.

### -param punkACL [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the string list object that generates candidates for the completed string. The object must expose an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface.

### -param pwszRegKeyPath [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional, null-terminated Unicode string that gives the registry path, including the value name, where the format string is stored as a <b>REG_SZ</b> value. The autocomplete object first looks for the path under <b>HKEY_CURRENT_USER</b>. If it fails, it tries <b>HKEY_LOCAL_MACHINE</b>. For a discussion of the format string, see the definition of <i>pwszQuickComplete</i>.

### -param pwszQuickComplete [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional null-terminated Unicode string that specifies the format to be used if the user enters text and presses CTRL+ENTER. Set this parameter to <b>NULL</b> to disable quick completion. Otherwise, the autocomplete object treats <i>pwszQuickComplete</i> as a <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a> format string and the text in the edit box as its associated argument, to produce a new string. For example, set <i>pwszQuickComplete</i> to "http://www.%s.com/". When a user enters "MyURL" into the edit box and presses CTRL+ENTER, the text in the edit box is updated to "http://www.MyURL.com/".

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">IAutoComplete</a>