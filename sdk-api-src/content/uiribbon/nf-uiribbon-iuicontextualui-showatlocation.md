---
UID: NF:uiribbon.IUIContextualUI.ShowAtLocation
title: IUIContextualUI::ShowAtLocation (uiribbon.h)
description: Displays a ContextPopup.
helpviewer_keywords: ["IUIContextualUI interface [Windows Ribbon]","ShowAtLocation method","IUIContextualUI.ShowAtLocation","IUIContextualUI::ShowAtLocation","ShowAtLocation","ShowAtLocation method [Windows Ribbon]","ShowAtLocation method [Windows Ribbon]","IUIContextualUI interface","scenicintent_IUIContextualUI_ShowAtLocation","uiribbon/IUIContextualUI::ShowAtLocation","windowsribbon.windowsribbon_iuicontextualui_showatlocation"]
old-location: windowsribbon\windowsribbon_iuicontextualui_showatlocation.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicontextualui\showatlocation.htm
ms.date: 12/05/2018
ms.keywords: IUIContextualUI interface [Windows Ribbon],ShowAtLocation method, IUIContextualUI.ShowAtLocation, IUIContextualUI::ShowAtLocation, ShowAtLocation, ShowAtLocation method [Windows Ribbon], ShowAtLocation method [Windows Ribbon],IUIContextualUI interface, scenicintent_IUIContextualUI_ShowAtLocation, uiribbon/IUIContextualUI::ShowAtLocation, windowsribbon.windowsribbon_iuicontextualui_showatlocation
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIContextualUI::ShowAtLocation
 - uiribbon/IUIContextualUI::ShowAtLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIContextualUI.ShowAtLocation
---

# IUIContextualUI::ShowAtLocation


## -description

Displays a <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextpopup">ContextPopup</a>.

## -parameters

### -param x

Type: <b>INT32</b>

The absolute x-coordinate, in screen coordinates, for the upper-left corner of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextpopup">ContextPopup</a>.

### -param y

Type: <b>INT32</b>

The absolute y-coordinate, in screen coordinates, for the upper-left corner of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextpopup">ContextPopup</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The location of the <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextpopup">ContextPopup</a> is not based on the screen coordinates of the application window or the mouse pointer.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-contextpopupsample">ContextPopup Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui">IUIContextualUI</a>