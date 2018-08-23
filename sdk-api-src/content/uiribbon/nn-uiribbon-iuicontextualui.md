---
UID: NN:uiribbon.IUIContextualUI
title: IUIContextualUI
author: windows-sdk-content
description: The IUIContextualUI interface is implemented by the Ribbon framework and provides the core functionality for the Context Popup View.
old-location: windowsribbon\windowsribbon_iuicontextualui.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicontextualui\iuicontextualui.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIContextualUI, IUIContextualUI interface [Windows Ribbon], IUIContextualUI interface [Windows Ribbon],described, scenicintent_IUIContextualUI, uiribbon/IUIContextualUI, windowsribbon.windowsribbon_iuicontextualui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiribbon.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUIContextualUI
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
req.product: Windows UI
---

# IUIContextualUI interface


## -description


The <b>IUIContextualUI</b> interface is implemented by the 
				Ribbon framework and provides the core functionality for the <a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a> View. 
			


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIContextualUI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIContextualUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIContextualUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd371486(v=VS.85).aspx">ShowAtLocation</a>
</td>
<td align="left" width="63%">
Displays a <a href="https://msdn.microsoft.com/en-us/library/Dd371654(v=VS.85).aspx">ContextPopup</a>.
		

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a> is composed of two components: the <a href="https://msdn.microsoft.com/en-us/library/Dd371651(v=VS.85).aspx">ContextMenu</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd371705(v=VS.85).aspx">MiniToolbar</a> elements.
			
				

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a> acts solely as a logical container for the <a href="https://msdn.microsoft.com/en-us/library/Dd371651(v=VS.85).aspx">ContextMenu</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd371705(v=VS.85).aspx">MiniToolbar</a>. It does not
				support scrolling, moving, or resizing. 
			</div>
<div> </div>
The <a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a> is typically displayed by right-clicking the mouse (or through the keyboard shortcut  SHIFT+F10) on an object of interest. The steps required to display the Context Popup are defined by the application.

The <a href="https://msdn.microsoft.com/en-us/library/Dd371651(v=VS.85).aspx">ContextMenu</a> is a list of menu items that is contextual and based on  
				the control clicked or the control with focus (when using the keyboard).
			

The <a href="https://msdn.microsoft.com/en-us/library/Dd371705(v=VS.85).aspx">MiniToolbar</a> is a floating toolbar that incorporates various Commands, galleries, and complex controls such as the <a href="https://msdn.microsoft.com/en-us/library/Dd940498(v=VS.85).aspx">Font Control</a> and the <a href="https://msdn.microsoft.com/en-us/library/Dd940492(v=VS.85).aspx">Combo Box</a>.
			

The following screen shot shows the <a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a> with a <a href="https://msdn.microsoft.com/en-us/library/Dd371651(v=VS.85).aspx">ContextMenu</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd371705(v=VS.85).aspx">MiniToolbar</a>.

<img alt="Screen shot with callouts showing the ContentPopup, ContextMenu, and MiniToolbar." src="images/Interfaces/IUIContextualUI_Concepts.png"/>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd940493(v=VS.85).aspx">Context Popup</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742701(v=VS.85).aspx">ContextPopup Sample</a>
 

 

