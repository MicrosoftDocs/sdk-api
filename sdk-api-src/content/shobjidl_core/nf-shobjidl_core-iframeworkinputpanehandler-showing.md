---
UID: NF:shobjidl_core.IFrameworkInputPaneHandler.Showing
title: IFrameworkInputPaneHandler::Showing (shobjidl_core.h)
description: Called before the input pane is shown, to allow the app window to make any necessary adjustments to its UI in response to the reduced screen space available to it.
helpviewer_keywords: ["IFrameworkInputPaneHandler interface [Windows Shell]","Showing method","IFrameworkInputPaneHandler.Showing","IFrameworkInputPaneHandler::Showing","Showing","Showing method [Windows Shell]","Showing method [Windows Shell]","IFrameworkInputPaneHandler interface","shell.IFrameworkInputPaneHandler_Showing","shobjidl_core/IFrameworkInputPaneHandler::Showing"]
old-location: shell\IFrameworkInputPaneHandler_Showing.htm
tech.root: shell
ms.assetid: E7CE2808-0146-4704-B1DA-1DDE691E946E
ms.date: 12/05/2018
ms.keywords: IFrameworkInputPaneHandler interface [Windows Shell],Showing method, IFrameworkInputPaneHandler.Showing, IFrameworkInputPaneHandler::Showing, Showing, Showing method [Windows Shell], Showing method [Windows Shell],IFrameworkInputPaneHandler interface, shell.IFrameworkInputPaneHandler_Showing, shobjidl_core/IFrameworkInputPaneHandler::Showing
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
 - IFrameworkInputPaneHandler::Showing
 - shobjidl_core/IFrameworkInputPaneHandler::Showing
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
 - IFrameworkInputPaneHandler.Showing
---

# IFrameworkInputPaneHandler::Showing


## -description

Called before the input pane is shown, to allow the app window to make any necessary adjustments to its UI in response to the reduced screen space available to it. This is particularly important for input elements, such as text boxes, that are used in conjunction with the input pane.

## -parameters

### -param prcInputPaneScreenLocation [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that supplies the screen coordinates that the input pane will occupy.

### -param fEnsureFocusedElementInView [in]

Type: <b>BOOL*</b>

A pointer to a value that is set to <b>true</b> if the app should attempt to keep its currently focused element (such as a text box) in view, which could require the app to move the element or rearrange its UI.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler">IFrameworkInputPaneHandler</a>