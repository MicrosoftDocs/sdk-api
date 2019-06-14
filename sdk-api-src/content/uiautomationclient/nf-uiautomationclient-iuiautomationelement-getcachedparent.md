---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedParent
title: IUIAutomationElement::GetCachedParent (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves from the cache the parent of this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedParent.htm
tech.root: WinAuto
ms.assetid: 10ca955b-416a-47c0-9970-940d98132b38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCachedParent, GetCachedParent method [Windows Accessibility], GetCachedParent method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedParent method, IUIAutomationElement.GetCachedParent, IUIAutomationElement::GetCachedParent, uiauto.uiauto_IUIAutomationElement_GetCachedParent, uiauto_IUIAutomationElement_GetCachedParent, uiautomationclient/IUIAutomationElement::GetCachedParent, winauto.uiauto_IUIAutomationElement_GetCachedParent
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
 - IUIAutomationElement.GetCachedParent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement::GetCachedParent


## -description


Retrieves from the cache the parent of this UI Automation element. 


## -parameters




### -param parent [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the cached parent element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedchildren">GetCachedChildren</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-treeoverview">UI Automation Tree Overview</a>
 

 

