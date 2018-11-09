---
UID: NF:uiautomationcore.ISpreadsheetProvider.GetItemByName
title: ISpreadsheetProvider::GetItemByName
author: windows-sdk-content
description: Exposes a UI Automation element that represents the spreadsheet cell that has the specified name.
old-location: winauto\uiauto_ISpreadsheetProvider_GetItemByName.htm
tech.root: WinAuto
ms.assetid: 9A496B3F-5095-4094-BAF6-D4EE20498D4B
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetItemByName, GetItemByName method [Windows Accessibility], GetItemByName method [Windows Accessibility],ISpreadsheetProvider interface, ISpreadsheetProvider interface [Windows Accessibility],GetItemByName method, ISpreadsheetProvider.GetItemByName, ISpreadsheetProvider::GetItemByName, uiautomationcore/ISpreadsheetProvider::GetItemByName, winauto.uiauto_ISpreadsheetProvider_GetItemByName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ISpreadsheetProvider.GetItemByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpreadsheetProvider::GetItemByName


## -description


Exposes a UI Automation element that represents the spreadsheet cell that has the specified name.  


## -parameters




### -param name [in]

Type: <b>LPCWSTR</b>

The name of the target cell.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives the element that represents the target cell. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A spreadsheet cell typically has a name such as “c5” or “a15”.  A name can also apply to a range of cells. 




## -see-also




<a href="https://msdn.microsoft.com/5D27761C-41F3-4908-B116-3ED9A379EA51">ISpreadsheetProvider</a>
 

 

