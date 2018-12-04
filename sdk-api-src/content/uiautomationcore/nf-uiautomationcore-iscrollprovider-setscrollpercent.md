---
UID: NF:uiautomationcore.IScrollProvider.SetScrollPercent
title: IScrollProvider::SetScrollPercent
author: windows-sdk-content
description: Sets the horizontal and vertical scroll position as a percentage of the total content area within the control.
old-location: winauto\uiauto_IScrollProvider_SetScrollPercent.htm
tech.root: WinAuto
ms.assetid: 4949fd00-6678-4278-b11b-cc8503e67de2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IScrollProvider interface [Windows Accessibility],SetScrollPercent method, IScrollProvider.SetScrollPercent, IScrollProvider::SetScrollPercent, SetScrollPercent, SetScrollPercent method [Windows Accessibility], SetScrollPercent method [Windows Accessibility],IScrollProvider interface, uiauto.uiauto_IScrollProvider_SetScrollPercent, uiauto_IScrollProvider_SetScrollPercent, uiautomationcore/IScrollProvider::SetScrollPercent, winauto.uiauto_IScrollProvider_SetScrollPercent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - IScrollProvider.SetScrollPercent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScrollProvider::SetScrollPercent


## -description


Sets the horizontal and vertical scroll position as a percentage of the total content area within the control.
        


## -parameters




### -param horizontalPercent [in]

Type: <b>double</b>

The horizontal position as a percentage of the content area's total range, or <b>UIA_ScrollPatternNoScroll</b> if there is no horizontal scrolling. 


### -param verticalPercent [in]

Type: <b>double</b>

The vertical position as a percentage of the content area's total range, or <b>UIA_ScrollPatternNoScroll</b> if there is no vertical scrolling. 



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is only useful when the content area of the control is 
            larger than the visible region. 
            




## -see-also




<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

