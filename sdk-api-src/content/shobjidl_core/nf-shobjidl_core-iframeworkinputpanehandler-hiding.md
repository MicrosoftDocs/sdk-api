---
UID: NF:shobjidl_core.IFrameworkInputPaneHandler.Hiding
title: IFrameworkInputPaneHandler::Hiding (shobjidl_core.h)
description: Called when the input pane is about to leave the display.
helpviewer_keywords: ["Hiding","Hiding method [Windows Shell]","Hiding method [Windows Shell]","IFrameworkInputPaneHandler interface","IFrameworkInputPaneHandler interface [Windows Shell]","Hiding method","IFrameworkInputPaneHandler.Hiding","IFrameworkInputPaneHandler::Hiding","shell.IFrameworkInputPaneHandler_Hiding","shobjidl_core/IFrameworkInputPaneHandler::Hiding"]
old-location: shell\IFrameworkInputPaneHandler_Hiding.htm
tech.root: shell
ms.assetid: B5182892-C40D-432c-9A84-F227A804D080
ms.date: 12/05/2018
ms.keywords: Hiding, Hiding method [Windows Shell], Hiding method [Windows Shell],IFrameworkInputPaneHandler interface, IFrameworkInputPaneHandler interface [Windows Shell],Hiding method, IFrameworkInputPaneHandler.Hiding, IFrameworkInputPaneHandler::Hiding, shell.IFrameworkInputPaneHandler_Hiding, shobjidl_core/IFrameworkInputPaneHandler::Hiding
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFrameworkInputPaneHandler::Hiding
 - shobjidl_core/IFrameworkInputPaneHandler::Hiding
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFrameworkInputPaneHandler.Hiding
---

# IFrameworkInputPaneHandler::Hiding


## -description

Called when the input pane is about to leave the display.

## -parameters

### -param fEnsureFocusedElementInView [in]

Type: <b>BOOL*</b>

A pointer to a value that is set to <b>true</b> if the app should attempt to keep its currently focused element (such as a text box) in view, which could require the app to rearrange its UI or move the element, usually back to its layout before the input pane was shown.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler">IFrameworkInputPaneHandler</a>