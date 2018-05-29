---
UID: NF:uiautomationclient.IUIAutomation.GetRootElement
title: IUIAutomation::GetRootElement
author: windows-sdk-content
description: Retrieves the UI Automation element that represents the desktop.
old-location: winauto\uiauto_IUIAutomation_GetRootElement.htm
old-project: WinAuto
ms.assetid: 9b6f3a78-a957-4ebd-a026-a8edb30faa88
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetRootElement, GetRootElement method [Windows Accessibility], GetRootElement method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetRootElement method, IUIAutomation.GetRootElement, IUIAutomation::GetRootElement, uiauto.uiauto_IUIAutomation_GetRootElement, uiauto_IUIAutomation_GetRootElement, uiautomationclient/IUIAutomation::GetRootElement, winauto.uiauto_IUIAutomation_GetRootElement
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
-	IUIAutomation.GetRootElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::GetRootElement


## -description


Retrieves the UI Automation element that represents the desktop.


## -parameters




### -param root [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the root element as a starting point for finding other elements, using the <a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a> and <a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a> methods.

When searching from the root element, be sure to specify <a href="uiauto_TreeScopeEnum.htm">TreeScope_Children</a> in the scope of the search, not <a href="uiauto_TreeScopeEnum.htm">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

			




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/0d2c0592-d29a-4e70-978e-55690aed82cb">IUIAutomation::GetRootElementBuildCache</a>
 

 

