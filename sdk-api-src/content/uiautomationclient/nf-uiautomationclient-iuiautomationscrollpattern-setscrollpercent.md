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

# IUIAutomationScrollPattern::SetScrollPercent


## -description


Sets the horizontal and vertical scroll positions as a percentage of the total content area within the UI Automation element.


## -parameters




### -param horizontalPercent [in]

Type: <b>double</b>

The percentage of the total horizontal content area, or <b>UIA_ScrollPatternNoScroll</b> if the horizontal position is not to be set.


### -param verticalPercent [in]

Type: <b>double</b>

The percentage of the total vertical content area, or <b>UIA_ScrollPatternNoScroll</b> if the vertical position is not to be set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is useful only when the content area of the control is larger than the visible region.




## -see-also




<a href="https://msdn.microsoft.com/cb62389c-5a7a-412d-a024-0ce9bc6403a2">IUIAutomationScrollPattern</a>



<a href="https://msdn.microsoft.com/2deb7399-604d-45eb-95d6-f1135550a18f">IUIAutomationScrollPattern::Scroll</a>
 

 

