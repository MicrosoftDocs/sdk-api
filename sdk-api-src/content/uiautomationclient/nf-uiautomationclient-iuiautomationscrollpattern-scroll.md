---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.Scroll
title: IUIAutomationScrollPattern::Scroll (uiautomationclient.h)
author: windows-sdk-content
description: Scrolls the visible region of the content area horizontally and vertically.
old-location: winauto\uiauto_IUIAutomationScrollPattern_Scroll.htm
tech.root: WinAuto
ms.assetid: 2deb7399-604d-45eb-95d6-f1135550a18f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationScrollPattern interface [Windows Accessibility],Scroll method, IUIAutomationScrollPattern.Scroll, IUIAutomationScrollPattern::Scroll, Scroll, Scroll method [Windows Accessibility], Scroll method [Windows Accessibility],IUIAutomationScrollPattern interface, uiauto.uiauto_IUIAutomationScrollPattern_Scroll, uiauto_IUIAutomationScrollPattern_Scroll, uiautomationclient/IUIAutomationScrollPattern::Scroll, winauto.uiauto_IUIAutomationScrollPattern_Scroll
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
 - IUIAutomationScrollPattern.Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationScrollPattern::Scroll


## -description


Scrolls the visible region of the content area horizontally and vertically.


## -parameters




### -param arg1 [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

A value indicating the size of the horizontal scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the horizontal position is not to be set.


### -param arg2 [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

A value from the <a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a> enumerated type indicating the size of the vertical scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the vertical position is not to be set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb62389c-5a7a-412d-a024-0ce9bc6403a2">IUIAutomationScrollPattern</a>



<a href="https://msdn.microsoft.com/2f31445d-6198-430a-8f31-3ff25b72581c">IUIAutomationScrollPattern::SetScrollPercent</a>
 

 

