---
UID: NF:uiautomationclient.IUIAutomationVirtualizedItemPattern.Realize
title: IUIAutomationVirtualizedItemPattern::Realize
author: windows-sdk-content
description: Creates a full UI Automation element for a virtualized item.
old-location: winauto\uiauto_IUIAutomationVirtualizedItemPattern_Realize.htm
tech.root: WinAuto
ms.assetid: 33831b88-cce7-47f3-acd1-e6b74f5a93d2
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IUIAutomationVirtualizedItemPattern interface [Windows Accessibility],Realize method, IUIAutomationVirtualizedItemPattern.Realize, IUIAutomationVirtualizedItemPattern::Realize, Realize, Realize method [Windows Accessibility], Realize method [Windows Accessibility],IUIAutomationVirtualizedItemPattern interface, uiauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize, uiauto_IUIAutomationVirtualizedItemPattern_Realize, uiautomationclient/IUIAutomationVirtualizedItemPattern::Realize, winauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize
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
 - IUIAutomationVirtualizedItemPattern.Realize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationVirtualizedItemPattern::Realize


## -description


Creates a full UI Automation element for a virtualized item.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A virtualized item is represented by a placeholder automation element in the UI Automation tree. The <b>Realize</b> method causes the provider to make full information available for the item so that a full UI Automation element can be created for the item. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/48f066f3-c78c-47a2-9668-ab79b1438130">IUIAutomationVirtualizedItemPattern</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52">Working with Virtualized Items</a>
 

 

