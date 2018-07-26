---
UID: NF:uiautomationclient.IUIAutomationGridPattern.GetItem
title: IUIAutomationGridPattern::GetItem
author: windows-sdk-content
description: Retrieves a UI Automation element representing an item in the grid.
old-location: winauto\uiauto_IUIAutomationGridPattern_GetItem.htm
old-project: WinAuto
ms.assetid: e18fd4ba-7fe2-4acb-97cd-c446d359dc38
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetItem, GetItem method [Windows Accessibility], GetItem method [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],GetItem method, IUIAutomationGridPattern.GetItem, IUIAutomationGridPattern::GetItem, uiauto.uiauto_IUIAutomationGridPattern_GetItem, uiauto_IUIAutomationGridPattern_GetItem, uiautomationclient/IUIAutomationGridPattern::GetItem, winauto.uiauto_IUIAutomationGridPattern_GetItem
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
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationGridPattern.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationGridPattern::GetItem


## -description


Retrieves a UI Automation element representing an item in the grid.


## -parameters




### -param row [in]

Type: <b>int</b>

The zero-based index of the row.


### -param column [in]

Type: <b>int</b>

The zero-based index of the column.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the element representing the grid item. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/36a4893e-5f49-413c-a29a-e58291c7d057">IUIAutomationGridPattern</a>
 

 

