---
UID: NN:shobjidl_core.IFrameworkInputPaneHandler
title: IFrameworkInputPaneHandler (shobjidl_core.h)
description: Enables an app to be notified when the input pane (the on-screen keyboard or handwriting panel) is being shown or hidden. This allows the app window to adjust its display so that no input areas (such as a text box) are obscured by the input pane.
helpviewer_keywords: ["IFrameworkInputPaneHandler","IFrameworkInputPaneHandler interface [Windows Shell]","IFrameworkInputPaneHandler interface [Windows Shell]","described","shell.IFrameworkInputPaneHandler","shobjidl_core/IFrameworkInputPaneHandler"]
old-location: shell\IFrameworkInputPaneHandler.htm
tech.root: shell
ms.assetid: E8038442-9E96-4eee-968E-3A6BC747852D
ms.date: 12/05/2018
ms.keywords: IFrameworkInputPaneHandler, IFrameworkInputPaneHandler interface [Windows Shell], IFrameworkInputPaneHandler interface [Windows Shell],described, shell.IFrameworkInputPaneHandler, shobjidl_core/IFrameworkInputPaneHandler
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
 - IFrameworkInputPaneHandler
 - shobjidl_core/IFrameworkInputPaneHandler
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
 - IFrameworkInputPaneHandler
---

# IFrameworkInputPaneHandler interface


## -description

Enables an app to be notified when the input pane (the on-screen keyboard or handwriting panel) is being shown or hidden. This allows the app window to adjust its display so that no input areas (such as a text box) are obscured by the input pane.

## -inheritance

The <b>IFrameworkInputPaneHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFrameworkInputPaneHandler</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface if your app needs to be informed when the input pane is shown or hidden, or its screen coordinates.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
