---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

