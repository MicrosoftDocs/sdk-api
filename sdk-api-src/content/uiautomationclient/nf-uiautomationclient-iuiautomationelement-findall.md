---
UID: NF:uiautomationclient.IUIAutomationElement.FindAll
title: IUIAutomationElement::FindAll (uiautomationclient.h)
description: Returns all UI Automation elements that satisfy the specified condition.
helpviewer_keywords: ["FindAll","FindAll method [Windows Accessibility]","FindAll method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","FindAll method","IUIAutomationElement.FindAll","IUIAutomationElement::FindAll","uiauto.uiauto_IUIAutomationElement_FindAll","uiauto_IUIAutomationElement_FindAll","uiautomationclient/IUIAutomationElement::FindAll","winauto.uiauto_IUIAutomationElement_FindAll"]
old-location: winauto\uiauto_IUIAutomationElement_FindAll.htm
tech.root: WinAuto
ms.assetid: ead73c6d-7fb8-4e00-b027-5d747268af08
ms.date: 12/05/2018
ms.keywords: FindAll, FindAll method [Windows Accessibility], FindAll method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],FindAll method, IUIAutomationElement.FindAll, IUIAutomationElement::FindAll, uiauto.uiauto_IUIAutomationElement_FindAll, uiauto_IUIAutomationElement_FindAll, uiautomationclient/IUIAutomationElement::FindAll, winauto.uiauto_IUIAutomationElement_FindAll
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
 - IUIAutomationElement::FindAll
 - uiautomationclient/IUIAutomationElement::FindAll
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
 - IUIAutomationElement.FindAll
---

# IUIAutomationElement::FindAll


## -description

Returns all UI Automation elements that satisfy the specified condition.

## -parameters

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

A combination of values specifying the scope of the search.

### -param condition [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a>*</b>

A pointer to a condition that represents the criteria to match.

### -param found [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The scope of the search is relative to the element on which the method is called. Elements are returned in the order in which they are encountered in the tree.

This function cannot search for ancestor elements in the Microsoft UI Automation tree; that is, <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Ancestors</a>  is not a valid value for the <i>scope</i> parameter.

When searching for top-level windows on the desktop, be sure to specify <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a> in the <i>scope</i> parameter, not <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<a href="/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<b>Reference</b>