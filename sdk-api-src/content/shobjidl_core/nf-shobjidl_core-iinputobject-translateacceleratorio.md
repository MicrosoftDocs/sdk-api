---
UID: NF:shobjidl_core.IInputObject.TranslateAcceleratorIO
title: IInputObject::TranslateAcceleratorIO (shobjidl_core.h)
description: Enables the object to process keyboard accelerators.
helpviewer_keywords: ["IInputObject interface [Windows Shell]","TranslateAcceleratorIO method","IInputObject.TranslateAcceleratorIO","IInputObject::TranslateAcceleratorIO","TranslateAcceleratorIO","TranslateAcceleratorIO method [Windows Shell]","TranslateAcceleratorIO method [Windows Shell]","IInputObject interface","_win32_IInputObject_TranslateAcceleratorIO","shell.IInputObject_TranslateAcceleratorIO","shobjidl_core/IInputObject::TranslateAcceleratorIO"]
old-location: shell\IInputObject_TranslateAcceleratorIO.htm
tech.root: shell
ms.assetid: e075556a-2910-41ee-a8f3-3fba1cd55a35
ms.date: 12/05/2018
ms.keywords: IInputObject interface [Windows Shell],TranslateAcceleratorIO method, IInputObject.TranslateAcceleratorIO, IInputObject::TranslateAcceleratorIO, TranslateAcceleratorIO, TranslateAcceleratorIO method [Windows Shell], TranslateAcceleratorIO method [Windows Shell],IInputObject interface, _win32_IInputObject_TranslateAcceleratorIO, shell.IInputObject_TranslateAcceleratorIO, shobjidl_core/IInputObject::TranslateAcceleratorIO
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
 - IInputObject::TranslateAcceleratorIO
 - shobjidl_core/IInputObject::TranslateAcceleratorIO
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
 - IInputObject.TranslateAcceleratorIO
---

# IInputObject::TranslateAcceleratorIO


## -description

Enables the object to process keyboard accelerators.

## -parameters

### -param pMsg

Type: <b>LPMSG</b>

The address of an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the keyboard message that is being translated.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the accelerator was translated, or <b>S_FALSE</b> otherwise.