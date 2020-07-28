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
f1_keywords:
- shobjidl_core/IFrameworkInputPaneHandler
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IFrameworkInputPaneHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFrameworkInputPaneHandler interface


## -description


Enables an app to be notified when the input pane (the on-screen keyboard or handwriting panel) is being shown or hidden. This allows the app window to adjust its display so that no input areas (such as a text box) are obscured by the input pane.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFrameworkInputPaneHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFrameworkInputPaneHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFrameworkInputPaneHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpanehandler-hiding">Hiding</a>
</td>
<td align="left" width="63%">
Called when the input pane is about to leave the display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpanehandler-showing">Showing</a>
</td>
<td align="left" width="63%">
Called before the input pane is shown, to allow the app window to make any necessary adjustments to its UI in response to the reduced screen space available to it. This is particularly important for input elements, such as text boxes, that are used in conjunction with the input pane.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface if your app needs to be informed when the input pane is shown or hidden, or its screen coordinates.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

