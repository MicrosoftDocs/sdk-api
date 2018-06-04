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

# IUIAutomationScrollPattern::Scroll


## -description


Scrolls the visible region of the content area horizontally and vertically.


## -parameters




### -param horizontalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

A value indicating the size of the horizontal scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the horizontal position is not to be set.


### -param verticalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

A value from the <a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a> enumerated type indicating the size of the vertical scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the vertical position is not to be set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb62389c-5a7a-412d-a024-0ce9bc6403a2">IUIAutomationScrollPattern</a>



<a href="https://msdn.microsoft.com/2f31445d-6198-430a-8f31-3ff25b72581c">IUIAutomationScrollPattern::SetScrollPercent</a>
 

 

