---
UID: NF:uiautomationclient.IUIAutomationTextRangeArray.GetElement
title: IUIAutomationTextRangeArray::GetElement
author: windows-sdk-content
description: Retrieves a text range from the collection.
old-location: winauto\uiauto_IUIAutomationTextRangeArray_GetElement.htm
old-project: WinAuto
ms.assetid: b5077152-b06a-4391-a0c2-013362014b2b
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetElement, GetElement method [Windows Accessibility], GetElement method [Windows Accessibility],IUIAutomationTextRangeArray interface, IUIAutomationTextRangeArray interface [Windows Accessibility],GetElement method, IUIAutomationTextRangeArray.GetElement, IUIAutomationTextRangeArray::GetElement, uiauto.uiauto_IUIAutomationTextRangeArray_GetElement, uiauto_IUIAutomationTextRangeArray_GetElement, uiautomationclient/IUIAutomationTextRangeArray::GetElement, winauto.uiauto_IUIAutomationTextRangeArray_GetElement
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationTextRangeArray.GetElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRangeArray::GetElement


## -description


Retrieves a text range from the collection.


## -parameters




### -param index [in]

Type: <b>int</b>

The zero-based index of the item.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9f059173-7539-4164-b7af-182fa851d11a">IUIAutomationTextRangeArray</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

