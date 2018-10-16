---
UID: NF:uiautomationcore.IScrollProvider.Scroll
title: IScrollProvider::Scroll
author: windows-sdk-content
description: Scrolls the visible region of the content area horizontally and vertically.
old-location: winauto\uiauto_IScrollProvider_Scroll.htm
tech.root: WinAuto
ms.assetid: d1bd15d2-beaf-4838-970a-00cfa2a7cfd9
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IScrollProvider interface [Windows Accessibility],Scroll method, IScrollProvider.Scroll, IScrollProvider::Scroll, Scroll, Scroll method [Windows Accessibility], Scroll method [Windows Accessibility],IScrollProvider interface, uiauto.uiauto_IScrollProvider_Scroll, uiauto_IScrollProvider_Scroll, uiautomationcore/IScrollProvider::Scroll, winauto.uiauto_IScrollProvider_Scroll
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
 - IScrollProvider.Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScrollProvider::Scroll


## -description


Scrolls the visible region of the content area horizontally and vertically.
        


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - horizontalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

The horizontal scrolling increment that is specific to the control.


#### - verticalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

The vertical scrolling increment that is specific to the control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

