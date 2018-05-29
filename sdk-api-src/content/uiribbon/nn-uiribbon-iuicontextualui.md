---
UID: NN:uiribbon.IUIContextualUI
title: IUIContextualUI
author: windows-sdk-content
description: The IUIContextualUI interface is implemented by the Ribbon framework and provides the core functionality for the Context Popup View.
old-location: windowsribbon\windowsribbon_iuicontextualui.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicontextualui\iuicontextualui.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IUIContextualUI, IUIContextualUI interface [Windows Ribbon], IUIContextualUI interface [Windows Ribbon],described, scenicintent_IUIContextualUI, uiribbon/IUIContextualUI, windowsribbon.windowsribbon_iuicontextualui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uiribbon.dll
api_name:
-	IUIContextualUI
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
				Ribbon framework and provides the core functionality for the <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> View. 
			


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
<a href="https://msdn.microsoft.com/90a78723-99c8-4d35-ba17-bacc609990e4">ShowAtLocation</a>
</td>
<td align="left" width="63%">

		Displays a <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>.
		

</td>
</tr>
</table> 


## -remarks




				The <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> is composed of two components: the <a href="https://msdn.microsoft.com/08cc0514-0795-4e6b-b80c-33d920783032">ContextMenu</a> and <a href="https://msdn.microsoft.com/bb50890d-554a-4add-a583-d4fd48b823bf">MiniToolbar</a> elements.
			
				

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> acts solely as a logical container for the <a href="https://msdn.microsoft.com/08cc0514-0795-4e6b-b80c-33d920783032">ContextMenu</a> and <a href="https://msdn.microsoft.com/bb50890d-554a-4add-a583-d4fd48b823bf">MiniToolbar</a>. It does not
				support scrolling, moving, or resizing. 
			</div>
<div> </div>
The <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> is typically displayed by right-clicking the mouse (or through the keyboard shortcut  SHIFT+F10) on an object of interest. The steps required to display the Context Popup are defined by the application.

The <a href="https://msdn.microsoft.com/08cc0514-0795-4e6b-b80c-33d920783032">ContextMenu</a> is a list of menu items that is contextual and based on  
				the control clicked or the control with focus (when using the keyboard).
			


				The <a href="https://msdn.microsoft.com/bb50890d-554a-4add-a583-d4fd48b823bf">MiniToolbar</a> is a floating toolbar that incorporates various Commands, galleries, and complex controls such as the <a href="https://msdn.microsoft.com/6052f2e3-2c9e-432e-9ed6-c1e3a50843d9">Font Control</a> and the <a href="https://msdn.microsoft.com/6b7de2ec-dcb7-44cb-b01f-db1ba0643499">Combo Box</a>.
			

The following screen shot shows the <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> with a <a href="https://msdn.microsoft.com/08cc0514-0795-4e6b-b80c-33d920783032">ContextMenu</a> and <a href="https://msdn.microsoft.com/bb50890d-554a-4add-a583-d4fd48b823bf">MiniToolbar</a>.

<img alt="Screen shot with callouts showing the ContentPopup, ContextMenu, and MiniToolbar." src="images/Interfaces/IUIContextualUI_Concepts.png"/>



## -see-also




<a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a>



<a href="https://msdn.microsoft.com/f334dbfc-710a-4652-b914-a668ae36aecd">ContextPopup Sample</a>
 

 

