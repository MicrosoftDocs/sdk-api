---
UID: NF:shobjidl_core.IInputObject.HasFocusIO
title: IInputObject::HasFocusIO (shobjidl_core.h)
description: Determines if one of the object's windows has the keyboard focus.
helpviewer_keywords: ["HasFocusIO","HasFocusIO method [Windows Shell]","HasFocusIO method [Windows Shell]","IInputObject interface","IInputObject interface [Windows Shell]","HasFocusIO method","IInputObject.HasFocusIO","IInputObject::HasFocusIO","_win32_IInputObject_HasFocusIO","shell.IInputObject_HasFocusIO","shobjidl_core/IInputObject::HasFocusIO"]
old-location: shell\IInputObject_HasFocusIO.htm
tech.root: shell
ms.assetid: f22f6b54-9d71-4451-81bf-6e3fd01ab36a
ms.date: 12/05/2018
ms.keywords: HasFocusIO, HasFocusIO method [Windows Shell], HasFocusIO method [Windows Shell],IInputObject interface, IInputObject interface [Windows Shell],HasFocusIO method, IInputObject.HasFocusIO, IInputObject::HasFocusIO, _win32_IInputObject_HasFocusIO, shell.IInputObject_HasFocusIO, shobjidl_core/IInputObject::HasFocusIO
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IInputObject::HasFocusIO
 - shobjidl_core/IInputObject::HasFocusIO
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
 - IInputObject.HasFocusIO
---

# IInputObject::HasFocusIO


## -description

Determines if one of the object's windows has the keyboard focus.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if one of the object's windows has the keyboard focus, or S_FALSE otherwise.

