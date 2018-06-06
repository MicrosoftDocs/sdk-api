---
UID: NF:uiautomationclient.IUIAutomationElementArray.GetElement
title: IUIAutomationElementArray::GetElement
author: windows-sdk-content
description: Retrieves a Microsoft UI Automation element from the collection.
old-location: winauto\uiauto_IUIAutomationElementArray_GetElement.htm
old-project: WinAuto
ms.assetid: c8651061-3a17-49d0-abc6-78ce3fa02363
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetElement, GetElement method [Windows Accessibility], GetElement method [Windows Accessibility],IUIAutomationElementArray interface, IUIAutomationElementArray interface [Windows Accessibility],GetElement method, IUIAutomationElementArray.GetElement, IUIAutomationElementArray::GetElement, uiauto.uiauto_IUIAutomationElementArray_GetElement, uiauto_IUIAutomationElementArray_GetElement, uiautomationclient/IUIAutomationElementArray::GetElement, winauto.uiauto_IUIAutomationElementArray_GetElement
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
 - IUIAutomationElementArray.GetElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElementArray::GetElement


## -description


Retrieves a Microsoft UI Automation element from the collection.


## -parameters




### -param index [in]

Type: <b>int</b>

The zero-based index of the element.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>
 

 

