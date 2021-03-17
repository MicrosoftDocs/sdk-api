---
UID: NF:shobjidl_core.IInputObjectSite.OnFocusChangeIS
title: IInputObjectSite::OnFocusChangeIS (shobjidl_core.h)
description: Informs the browser that the focus has changed.
helpviewer_keywords: ["IInputObjectSite interface [Windows Shell]","OnFocusChangeIS method","IInputObjectSite.OnFocusChangeIS","IInputObjectSite::OnFocusChangeIS","OnFocusChangeIS","OnFocusChangeIS method [Windows Shell]","OnFocusChangeIS method [Windows Shell]","IInputObjectSite interface","_win32_IInputObjectSite_OnFocusChangeIS","shell.IInputObjectSite_OnFocusChangeIS","shobjidl_core/IInputObjectSite::OnFocusChangeIS"]
old-location: shell\IInputObjectSite_OnFocusChangeIS.htm
tech.root: shell
ms.assetid: b779beea-534b-4cf0-9426-db2bbcb52277
ms.date: 12/05/2018
ms.keywords: IInputObjectSite interface [Windows Shell],OnFocusChangeIS method, IInputObjectSite.OnFocusChangeIS, IInputObjectSite::OnFocusChangeIS, OnFocusChangeIS, OnFocusChangeIS method [Windows Shell], OnFocusChangeIS method [Windows Shell],IInputObjectSite interface, _win32_IInputObjectSite_OnFocusChangeIS, shell.IInputObjectSite_OnFocusChangeIS, shobjidl_core/IInputObjectSite::OnFocusChangeIS
req.header: shobjidl_core.h
req.include-header: Shlobj.h
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
 - IInputObjectSite::OnFocusChangeIS
 - shobjidl_core/IInputObjectSite::OnFocusChangeIS
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
 - IInputObjectSite.OnFocusChangeIS
---

# IInputObjectSite::OnFocusChangeIS


## -description

Informs the browser that the focus has changed.

## -parameters

### -param punkObj

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object gaining or losing the focus.

### -param fSetFocus

Type: <b>BOOL</b>

Indicates if the object has gained or lost the focus. If this value is nonzero, the object has gained the focus. If this value is zero, the object has lost the focus.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the method was successful, or a COM-defined error code otherwise.

## -remarks

The calling object should call this method whenever one of its windows gains or loses the input focus.