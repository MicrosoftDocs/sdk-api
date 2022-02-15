---
UID: NN:uiribbon.IUIContextualUI
title: IUIContextualUI (uiribbon.h)
description: The IUIContextualUI interface is implemented by the Ribbon framework and provides the core functionality for the Context Popup View.
helpviewer_keywords: ["IUIContextualUI","IUIContextualUI interface [Windows Ribbon]","IUIContextualUI interface [Windows Ribbon]","described","scenicintent_IUIContextualUI","uiribbon/IUIContextualUI","windowsribbon.windowsribbon_iuicontextualui"]
old-location: windowsribbon\windowsribbon_iuicontextualui.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicontextualui\iuicontextualui.htm
ms.date: 12/05/2018
ms.keywords: IUIContextualUI, IUIContextualUI interface [Windows Ribbon], IUIContextualUI interface [Windows Ribbon],described, scenicintent_IUIContextualUI, uiribbon/IUIContextualUI, windowsribbon.windowsribbon_iuicontextualui
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
req.dll: Uiribbon.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIContextualUI
 - uiribbon/IUIContextualUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUIContextualUI
---

# IUIContextualUI interface


## -description

The <b>IUIContextualUI</b> interface is implemented by the 
				Ribbon framework and provides the core functionality for the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> View.

## -inheritance

The <b>IUIContextualUI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIContextualUI</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> is composed of two components: the <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextmenu">ContextMenu</a> and <a href="/windows/desktop/windowsribbon/windowsribbon-element-minitoolbar">MiniToolbar</a> elements.
			
				

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> acts solely as a logical container for the <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextmenu">ContextMenu</a> and <a href="/windows/desktop/windowsribbon/windowsribbon-element-minitoolbar">MiniToolbar</a>. It does not
				support scrolling, moving, or resizing. 
			</div>
<div> </div>
The <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> is typically displayed by right-clicking the mouse (or through the keyboard shortcut  SHIFT+F10) on an object of interest. The steps required to display the Context Popup are defined by the application.

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextmenu">ContextMenu</a> is a list of menu items that is contextual and based on  
				the control clicked or the control with focus (when using the keyboard).
			

The <a href="/windows/desktop/windowsribbon/windowsribbon-element-minitoolbar">MiniToolbar</a> is a floating toolbar that incorporates various Commands, galleries, and complex controls such as the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-fontcontrol">Font Control</a> and the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-combobox">Combo Box</a>.
			

The following screen shot shows the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a> with a <a href="/windows/desktop/windowsribbon/windowsribbon-element-contextmenu">ContextMenu</a> and <a href="/windows/desktop/windowsribbon/windowsribbon-element-minitoolbar">MiniToolbar</a>.

<img alt="Screen shot with callouts showing the ContentPopup, ContextMenu, and MiniToolbar." src="./images/IUIContextualUI_Concepts.png"/>

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-controls-contextpopup">Context Popup</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-contextpopupsample">ContextPopup Sample</a>
