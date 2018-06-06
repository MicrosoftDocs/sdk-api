---
UID: NF:uiautomationclient.IUIAutomationGridPattern.get_CachedRowCount
title: IUIAutomationGridPattern::get_CachedRowCount
author: windows-sdk-content
description: Retrieves the cached number of rows in the grid.
old-location: winauto\uiauto_IUIAutomationGridPattern_CachedRowCount.htm
old-project: WinAuto
ms.assetid: 783e48e4-c554-4bc9-bf36-3fcc35d00d22
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: CachedRowCount property [Windows Accessibility], CachedRowCount property [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],CachedRowCount property, IUIAutomationGridPattern.CachedRowCount, IUIAutomationGridPattern.get_CachedRowCount, IUIAutomationGridPattern::CachedRowCount, IUIAutomationGridPattern::get_CachedRowCount, get_CachedRowCount, uiauto.uiauto_IUIAutomationGridPattern_CachedRowCount, uiauto_IUIAutomationGridPattern_CachedRowCount, uiautomationclient/IUIAutomationGridPattern::CachedRowCount, uiautomationclient/IUIAutomationGridPattern::get_CachedRowCount, winauto.uiauto_IUIAutomationGridPattern_CachedRowCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationGridPattern.CachedRowCount
 - IUIAutomationGridPattern.get_CachedRowCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationGridPattern::get_CachedRowCount


## -description


Retrieves the cached number of rows in the grid.

This property is read-only.


## -parameters


## -remarks



Hidden rows and columns, depending on the provider implementation, may be loaded in the Microsoft UI Automation tree and will therefore be reflected in the row count and column count properties. If the hidden rows and columns have not yet been loaded they are not counted.




## -see-also




<a href="https://msdn.microsoft.com/36a4893e-5f49-413c-a29a-e58291c7d057">IUIAutomationGridPattern</a>
 

 

