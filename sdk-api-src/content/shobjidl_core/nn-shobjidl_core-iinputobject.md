---
UID: NN:shobjidl_core.IInputObject
title: IInputObject (shobjidl_core.h)
description: Exposes methods that change UI activation and process accelerators for a user input object contained in the Shell.
helpviewer_keywords: ["IInputObject","IInputObject interface [Windows Shell]","IInputObject interface [Windows Shell]","described","_win32_IInputObject","shell.IInputObject","shobjidl_core/IInputObject"]
old-location: shell\IInputObject.htm
tech.root: shell
ms.assetid: 5fbbcd26-c60a-4b6a-92cf-36b8bd429266
ms.date: 12/05/2018
ms.keywords: IInputObject, IInputObject interface [Windows Shell], IInputObject interface [Windows Shell],described, _win32_IInputObject, shell.IInputObject, shobjidl_core/IInputObject
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IInputObject
 - shobjidl_core/IInputObject
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
 - IInputObject
---

# IInputObject interface


## -description

Exposes methods that change UI activation and process accelerators for a user input object contained in the Shell.

## -inheritance

The <b>IInputObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInputObject</b> also has these types of members:

## -remarks

Implement <b>IInputObject</b> if you are implementing a Shell object that takes user input.

You do not call this interface directly. <b>IInputObject</b> is used by the Shell or the browser to notify the object of UI activation changes and to translate keyboard accelerators.

<b>IInputObject</b> is derived from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. The listed methods are specific to <b>IInputObject</b>.
