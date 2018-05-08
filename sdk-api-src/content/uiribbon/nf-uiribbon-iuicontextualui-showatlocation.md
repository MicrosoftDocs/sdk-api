---
UID: NF:uiribbon.IUIContextualUI.ShowAtLocation
title: IUIContextualUI::ShowAtLocation
author: windows-driver-content
description: Displays a ContextPopup.
old-location: windowsribbon\windowsribbon_iuicontextualui_showatlocation.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicontextualui\showatlocation.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IUIContextualUI interface [Windows Ribbon],ShowAtLocation method, IUIContextualUI.ShowAtLocation, IUIContextualUI::ShowAtLocation, ShowAtLocation, ShowAtLocation method [Windows Ribbon], ShowAtLocation method [Windows Ribbon],IUIContextualUI interface, scenicintent_IUIContextualUI_ShowAtLocation, uiribbon/IUIContextualUI::ShowAtLocation, windowsribbon.windowsribbon_iuicontextualui_showatlocation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mshtml.dll
api_name:
-	IUIContextualUI.ShowAtLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIContextualUI::ShowAtLocation


## -description



		Displays a <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>.
		


## -parameters




### -param x

Type: <b>INT32</b>


					The absolute x-coordinate, in screen coordinates, for the upper-left corner of the <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>. 				
				


### -param y

Type: <b>INT32</b>


					The absolute y-coordinate, in screen coordinates, for the upper-left corner of the <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>. 				
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				The location of the <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a> is not based on the screen coordinates of the application window or the mouse pointer.
			




## -see-also




<a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a>



<a href="https://msdn.microsoft.com/f334dbfc-710a-4652-b914-a668ae36aecd">ContextPopup Sample</a>



<a href="https://msdn.microsoft.com/dbefd3e0-bb47-41df-b164-b2f279380e36">IUIContextualUI</a>
 

 

