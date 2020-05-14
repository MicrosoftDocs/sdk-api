---
UID: NF:uiautomationclient.IUIAutomation.GetRootElement
title: IUIAutomation::GetRootElement (uiautomationclient.h)
description: Retrieves the UI Automation element that represents the desktop.helpviewer_keywords: ["GetRootElement","GetRootElement method [Windows Accessibility]","GetRootElement method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","GetRootElement method","IUIAutomation.GetRootElement","IUIAutomation::GetRootElement","uiauto.uiauto_IUIAutomation_GetRootElement","uiauto_IUIAutomation_GetRootElement","uiautomationclient/IUIAutomation::GetRootElement","winauto.uiauto_IUIAutomation_GetRootElement"]
old-location: winauto\uiauto_IUIAutomation_GetRootElement.htm
tech.root: WinAuto
ms.assetid: 9b6f3a78-a957-4ebd-a026-a8edb30faa88
ms.date: 12/05/2018
ms.keywords: GetRootElement, GetRootElement method [Windows Accessibility], GetRootElement method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetRootElement method, IUIAutomation.GetRootElement, IUIAutomation::GetRootElement, uiauto.uiauto_IUIAutomation_GetRootElement, uiauto_IUIAutomation_GetRootElement, uiautomationclient/IUIAutomation::GetRootElement, winauto.uiauto_IUIAutomation_GetRootElement
f1_keywords:
- uiautomationclient/IUIAutomation.GetRootElement
dev_langs:
- c++
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
- IUIAutomation.GetRootElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::GetRootElement


## -description


Retrieves the UI Automation element that represents the desktop.


## -parameters




### -param root [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the root element as a starting point for finding other elements, using the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a> and <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a> methods.

When searching from the root element, be sure to specify <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a> in the scope of the search, not <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache">IUIAutomation::GetRootElementBuildCache</a>
 

 

