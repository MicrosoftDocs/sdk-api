---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.SetScrollPercent
title: IUIAutomationScrollPattern::SetScrollPercent
author: windows-sdk-content
description: Sets the horizontal and vertical scroll positions as a percentage of the total content area within the UI Automation element.
old-location: winauto\uiauto_IUIAutomationScrollPattern_SetScrollPercent.htm
tech.root: WinAuto
ms.assetid: 2f31445d-6198-430a-8f31-3ff25b72581c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUIAutomationScrollPattern interface [Windows Accessibility],SetScrollPercent method, IUIAutomationScrollPattern.SetScrollPercent, IUIAutomationScrollPattern::SetScrollPercent, SetScrollPercent, SetScrollPercent method [Windows Accessibility], SetScrollPercent method [Windows Accessibility],IUIAutomationScrollPattern interface, uiauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent, uiauto_IUIAutomationScrollPattern_SetScrollPercent, uiautomationclient/IUIAutomationScrollPattern::SetScrollPercent, winauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomationScrollPattern.SetScrollPercent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

