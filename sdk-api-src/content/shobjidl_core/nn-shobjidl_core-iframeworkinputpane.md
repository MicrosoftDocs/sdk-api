---
UID: NN:shobjidl_core.IFrameworkInputPane
title: IFrameworkInputPane (shobjidl_core.h)
description: Provides methods that enable apps to be informed of state changes and location for the input pane.
helpviewer_keywords: ["IFrameworkInputPane","IFrameworkInputPane interface [Windows Shell]","IFrameworkInputPane interface [Windows Shell]","described","shell.IFrameworkInputPane","shobjidl_core/IFrameworkInputPane"]
old-location: shell\IFrameworkInputPane.htm
tech.root: shell
ms.assetid: 05C115BA-249A-4271-9C6F-DAAEE91BB936
ms.date: 12/05/2018
ms.keywords: IFrameworkInputPane, IFrameworkInputPane interface [Windows Shell], IFrameworkInputPane interface [Windows Shell],described, shell.IFrameworkInputPane, shobjidl_core/IFrameworkInputPane
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFrameworkInputPane
 - shobjidl_core/IFrameworkInputPane
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
 - IFrameworkInputPane
---

# IFrameworkInputPane interface


## -description

Provides methods that enable apps to be informed of state changes and location for the input pane. The input pane is a UI element, an on-screen keyboard or handwriting panel, that appears when the user performs an action that requires them to enter information, such as selecting a search box or an entry field in a form. Apps can then adjust their UI so that the input pane does not obscure items that the user might need to access while the input pane is shown.

## -inheritance

The <b>IFrameworkInputPane</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFrameworkInputPane</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface; the implementation is supplied with Windows as CLSID_FrameworkInputPane.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
