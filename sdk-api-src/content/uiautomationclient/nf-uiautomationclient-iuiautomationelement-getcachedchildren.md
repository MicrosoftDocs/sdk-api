---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedChildren
title: IUIAutomationElement::GetCachedChildren (uiautomationclient.h)
description: Retrieves the cached child elements of this UI Automation element.
helpviewer_keywords: ["GetCachedChildren","GetCachedChildren method [Windows Accessibility]","GetCachedChildren method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetCachedChildren method","IUIAutomationElement.GetCachedChildren","IUIAutomationElement::GetCachedChildren","uiauto.uiauto_IUIAutomationElement_GetCachedChildren","uiauto_IUIAutomationElement_GetCachedChildren","uiautomationclient/IUIAutomationElement::GetCachedChildren","winauto.uiauto_IUIAutomationElement_GetCachedChildren"]
old-location: winauto\uiauto_IUIAutomationElement_GetCachedChildren.htm
tech.root: WinAuto
ms.assetid: dab24be3-0e0e-445f-a9cc-bb2733916cdc
ms.date: 12/05/2018
ms.keywords: GetCachedChildren, GetCachedChildren method [Windows Accessibility], GetCachedChildren method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedChildren method, IUIAutomationElement.GetCachedChildren, IUIAutomationElement::GetCachedChildren, uiauto.uiauto_IUIAutomationElement_GetCachedChildren, uiauto_IUIAutomationElement_GetCachedChildren, uiautomationclient/IUIAutomationElement::GetCachedChildren, winauto.uiauto_IUIAutomationElement_GetCachedChildren
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
 - IUIAutomationElement::GetCachedChildren
 - uiautomationclient/IUIAutomationElement::GetCachedChildren
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
 - IUIAutomationElement.GetCachedChildren
---

# IUIAutomationElement::GetCachedChildren


## -description

Retrieves the cached child elements of this UI Automation element.

## -parameters

### -param children [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to a collection of the cached child elements.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The view of the returned collection is determined by the TreeFilter property of the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> that was active when this element was obtained.

Children are cached only if the scope of the cache request included <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Subtree</a>, <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a>, or <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>.

If the cache request specified that children were to be cached at this level, but there are no children, the value of this property is 0. However, if no request was made to cache children at this level, an attempt to retrieve the property returns an error.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedparent">GetCachedParent</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<a href="/windows/desktop/WinAuto/uiauto-obtainingelements">Obtaining UI Automation Elements</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-treeoverview">UI Automation Tree Overview</a>