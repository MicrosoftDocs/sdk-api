---
UID: NF:uiautomationclient.IUIAutomationElement.FindAllBuildCache
title: IUIAutomationElement::FindAllBuildCache (uiautomationclient.h)
description: Returns all UI Automation elements that satisfy the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["FindAllBuildCache","FindAllBuildCache method [Windows Accessibility]","FindAllBuildCache method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","FindAllBuildCache method","IUIAutomationElement.FindAllBuildCache","IUIAutomationElement::FindAllBuildCache","uiauto.uiauto_IUIAutomationElement_FindAllBuildCache","uiauto_IUIAutomationElement_FindAllBuildCache","uiautomationclient/IUIAutomationElement::FindAllBuildCache","winauto.uiauto_IUIAutomationElement_FindAllBuildCache"]
old-location: winauto\uiauto_IUIAutomationElement_FindAllBuildCache.htm
tech.root: WinAuto
ms.assetid: acf16f88-2b68-4fd4-b715-b3a61340bdd0
ms.date: 12/05/2018
ms.keywords: FindAllBuildCache, FindAllBuildCache method [Windows Accessibility], FindAllBuildCache method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],FindAllBuildCache method, IUIAutomationElement.FindAllBuildCache, IUIAutomationElement::FindAllBuildCache, uiauto.uiauto_IUIAutomationElement_FindAllBuildCache, uiauto_IUIAutomationElement_FindAllBuildCache, uiautomationclient/IUIAutomationElement::FindAllBuildCache, winauto.uiauto_IUIAutomationElement_FindAllBuildCache
f1_keywords:
- uiautomationclient/IUIAutomationElement.FindAllBuildCache
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
- IUIAutomationElement.FindAllBuildCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement::FindAllBuildCache


## -description


Returns all UI Automation elements that satisfy the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param arg1 [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

A combination of values specifying the scope of the search.


### -param condition [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to a condition that represents the criteria to match.


### -param cacheRequest [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the control patterns and properties to include in the cache.


### -param found [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to an array of matching elements. If there are no matches, <b>NULL</b> is returned. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The scope of the search is relative to the element on which the method is called. Elements are returned in the order in which they were encountered in the tree.

This function cannot search for ancestor elements in the Microsoft UI Automation tree; that is, <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Ancestors</a>  is not a valid value for the <i>scope</i> parameter.

When searching for top-level windows on the desktop, be sure to specify <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a> in the <i>scope</i> parameter, not <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<b>Reference</b>
 

 

