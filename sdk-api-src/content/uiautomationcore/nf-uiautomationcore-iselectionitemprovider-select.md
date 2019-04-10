---
UID: NF:uiautomationcore.ISelectionItemProvider.Select
title: ISelectionItemProvider::Select (uiautomationcore.h)
author: windows-sdk-content
description: Deselects any selected items and then selects the current element.
old-location: winauto\uiauto_ISelectionItemProvider_Select.htm
tech.root: WinAuto
ms.assetid: b11e3472-e7dc-462d-93f4-e02f07ebd45f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISelectionItemProvider interface [Windows Accessibility],Select method, ISelectionItemProvider.Select, ISelectionItemProvider::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],ISelectionItemProvider interface, uiauto.uiauto_ISelectionItemProvider_Select, uiauto_ISelectionItemProvider_Select, uiautomationcore/ISelectionItemProvider::Select, winauto.uiauto_ISelectionItemProvider_Select
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
 - ISelectionItemProvider.Select
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISelectionItemProvider::Select


## -description


Deselects any selected items and then selects the current element. 


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the current element isn’t selected, this method deselects any selected items and then selects the current element.  If the current element is already selected, this method does nothing.




## -see-also




<a href="https://msdn.microsoft.com/464b05e3-06da-44b9-b4a6-c64452fcdb6d">ISelectionItemProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

