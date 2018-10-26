---
UID: NF:uiautomationclient.IUIAutomationGridPattern.get_CurrentRowCount
title: IUIAutomationGridPattern::get_CurrentRowCount
author: windows-sdk-content
description: Retrieves the number of rows in the grid.
old-location: winauto\uiauto_IUIAutomationGridPattern_CurrentRowCount.htm
tech.root: WinAuto
ms.assetid: 6ca5c2f0-f183-4cc9-9446-08da834ba903
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CurrentRowCount property [Windows Accessibility], CurrentRowCount property [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],CurrentRowCount property, IUIAutomationGridPattern.CurrentRowCount, IUIAutomationGridPattern.get_CurrentRowCount, IUIAutomationGridPattern::CurrentRowCount, IUIAutomationGridPattern::get_CurrentRowCount, get_CurrentRowCount, uiauto.uiauto_IUIAutomationGridPattern_CurrentRowCount, uiauto_IUIAutomationGridPattern_CurrentRowCount, uiautomationclient/IUIAutomationGridPattern::CurrentRowCount, uiautomationclient/IUIAutomationGridPattern::get_CurrentRowCount, winauto.uiauto_IUIAutomationGridPattern_CurrentRowCount
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
 - IUIAutomationGridPattern.CurrentRowCount
 - IUIAutomationGridPattern.get_CurrentRowCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationGridPattern::get_CurrentRowCount


## -description


Retrieves the number of rows in the grid.

This property is read-only.


## -parameters


## -remarks



Hidden rows and columns, depending on the provider implementation, may be loaded in the Microsoft UI Automation tree and will therefore be reflected in the row count and column count properties. If the hidden rows and columns have not yet been loaded they are not counted.




## -see-also




<a href="https://msdn.microsoft.com/36a4893e-5f49-413c-a29a-e58291c7d057">IUIAutomationGridPattern</a>
 

 

