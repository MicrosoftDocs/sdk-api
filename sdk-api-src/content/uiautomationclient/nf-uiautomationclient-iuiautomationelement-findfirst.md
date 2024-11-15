---
UID: NF:uiautomationclient.IUIAutomationElement.FindFirst
title: IUIAutomationElement::FindFirst (uiautomationclient.h)
description: Retrieves the first child or descendant element that matches the specified condition.
helpviewer_keywords: ["FindFirst","FindFirst method [Windows Accessibility]","FindFirst method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","FindFirst method","IUIAutomationElement.FindFirst","IUIAutomationElement::FindFirst","uiauto.uiauto_IUIAutomationElement_FindFirst","uiauto_IUIAutomationElement_FindFirst","uiautomationclient/IUIAutomationElement::FindFirst","winauto.uiauto_IUIAutomationElement_FindFirst"]
old-location: winauto\uiauto_IUIAutomationElement_FindFirst.htm
tech.root: WinAuto
ms.assetid: 84098431-46e8-49bd-a258-337ad1d68f91
ms.date: 12/05/2018
ms.keywords: FindFirst, FindFirst method [Windows Accessibility], FindFirst method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],FindFirst method, IUIAutomationElement.FindFirst, IUIAutomationElement::FindFirst, uiauto.uiauto_IUIAutomationElement_FindFirst, uiauto_IUIAutomationElement_FindFirst, uiautomationclient/IUIAutomationElement::FindFirst, winauto.uiauto_IUIAutomationElement_FindFirst
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement::FindFirst
 - uiautomationclient/IUIAutomationElement::FindFirst
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement.FindFirst
---

# IUIAutomationElement::FindFirst


## -description

Retrieves the first child or descendant element that matches the specified condition.

## -parameters

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

A combination of values specifying the scope of the search.

### -param condition [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to a condition that represents the criteria to match.

### -param found [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the element. <b>NULL</b> is returned if no matching element is found.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The scope of the search is relative to the element on which the method is called. Elements are returned in the order in which they were encountered in the tree.

This function cannot search for ancestor elements in the Microsoft UI Automation tree; that is, <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Ancestors</a>  is not a valid value for the <i>scope</i> parameter.

When searching for top-level windows on the desktop, be sure to specify <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a> in the <i>scope</i> parameter, not <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.

This function ignores elements in the raw tree. Call <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a> to search the raw tree by specifying the appropriate <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a> on the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> passed to that function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<a href="/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<b>Reference</b>