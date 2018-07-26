---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetPattern.GetItemByName
title: IUIAutomationSpreadsheetPattern::GetItemByName
author: windows-sdk-content
description: Retrieves a UI Automation element that represents the spreadsheet cell that has the specified name.
old-location: winauto\uiauto_IUIAutomationSpreadsheetPattern_GetItemByName.htm
old-project: WinAuto
ms.assetid: 4CDE57FA-1B94-408E-B1E6-3CD3CFC5AB82
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetItemByName, GetItemByName method [Windows Accessibility], GetItemByName method [Windows Accessibility],IUIAutomationSpreadsheetPattern interface, IUIAutomationSpreadsheetPattern interface [Windows Accessibility],GetItemByName method, IUIAutomationSpreadsheetPattern.GetItemByName, IUIAutomationSpreadsheetPattern::GetItemByName, uiautomationclient/IUIAutomationSpreadsheetPattern::GetItemByName, winauto.uiauto_IUIAutomationSpreadsheetPattern_GetItemByName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationSpreadsheetPattern.GetItemByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationSpreadsheetPattern::GetItemByName


## -description


Retrieves a UI Automation element that represents the spreadsheet cell that has the specified name.  




## -parameters




### -param name [in]

Type: <b>BSTR</b>

The name of the target cell.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives the element that represents the target cell.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/049DC33E-48C3-43AB-A5B0-401CDBAE4873">IUIAutomationSpreadsheetPattern</a>
 

 

