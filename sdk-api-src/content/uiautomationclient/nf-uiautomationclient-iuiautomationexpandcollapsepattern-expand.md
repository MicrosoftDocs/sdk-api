---
UID: NF:uiautomationclient.IUIAutomationExpandCollapsePattern.Expand
title: IUIAutomationExpandCollapsePattern::Expand (uiautomationclient.h)
description: Displays all child nodes, controls, or content of the element.
helpviewer_keywords: ["Expand","Expand method [Windows Accessibility]","Expand method [Windows Accessibility]","IUIAutomationExpandCollapsePattern interface","IUIAutomationExpandCollapsePattern interface [Windows Accessibility]","Expand method","IUIAutomationExpandCollapsePattern.Expand","IUIAutomationExpandCollapsePattern::Expand","uiauto.uiauto_IUIAutomationExpandCollapsePattern_Expand","uiauto_IUIAutomationExpandCollapsePattern_Expand","uiautomationclient/IUIAutomationExpandCollapsePattern::Expand","winauto.uiauto_IUIAutomationExpandCollapsePattern_Expand"]
old-location: winauto\uiauto_IUIAutomationExpandCollapsePattern_Expand.htm
tech.root: WinAuto
ms.assetid: bc21cffc-63fe-4c5d-9c4d-35e1bab67a7c
ms.date: 12/05/2018
ms.keywords: Expand, Expand method [Windows Accessibility], Expand method [Windows Accessibility],IUIAutomationExpandCollapsePattern interface, IUIAutomationExpandCollapsePattern interface [Windows Accessibility],Expand method, IUIAutomationExpandCollapsePattern.Expand, IUIAutomationExpandCollapsePattern::Expand, uiauto.uiauto_IUIAutomationExpandCollapsePattern_Expand, uiauto_IUIAutomationExpandCollapsePattern_Expand, uiautomationclient/IUIAutomationExpandCollapsePattern::Expand, winauto.uiauto_IUIAutomationExpandCollapsePattern_Expand
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
 - IUIAutomationExpandCollapsePattern::Expand
 - uiautomationclient/IUIAutomationExpandCollapsePattern::Expand
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
 - IUIAutomationExpandCollapsePattern.Expand
---

# IUIAutomationExpandCollapsePattern::Expand


## -description

Displays all child nodes, controls, or content of the element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is a blocking method that returns after the element has been expanded.

There are cases when a element that is marked as a leaf node might not know whether it has children until either the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse">IUIAutomationExpandCollapsePattern::Collapse</a> or the <b>IUIAutomationExpandCollapsePattern::Expand</b> method is called. This behavior is possible with a tree view control that does delayed loading of its child items. For example, Microsoft Windows Explorer might display the expand icon for a node even though there are currently no child items; when the icon is clicked, the control polls for child items, finds none, and removes the expand icon. In these cases clients should listen for a property-changed event on the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-get_currentexpandcollapsestate">IUIAutomationExpandCollapsePattern::CurrentExpandCollapseState</a> property.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationexpandcollapsepattern">IUIAutomationExpandCollapsePattern</a>
