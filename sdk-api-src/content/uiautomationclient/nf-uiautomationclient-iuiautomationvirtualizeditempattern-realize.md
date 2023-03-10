---
UID: NF:uiautomationclient.IUIAutomationVirtualizedItemPattern.Realize
title: IUIAutomationVirtualizedItemPattern::Realize (uiautomationclient.h)
description: Creates a full UI Automation element for a virtualized item.
helpviewer_keywords: ["IUIAutomationVirtualizedItemPattern interface [Windows Accessibility]","Realize method","IUIAutomationVirtualizedItemPattern.Realize","IUIAutomationVirtualizedItemPattern::Realize","Realize","Realize method [Windows Accessibility]","Realize method [Windows Accessibility]","IUIAutomationVirtualizedItemPattern interface","uiauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize","uiauto_IUIAutomationVirtualizedItemPattern_Realize","uiautomationclient/IUIAutomationVirtualizedItemPattern::Realize","winauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize"]
old-location: winauto\uiauto_IUIAutomationVirtualizedItemPattern_Realize.htm
tech.root: WinAuto
ms.assetid: 33831b88-cce7-47f3-acd1-e6b74f5a93d2
ms.date: 12/05/2018
ms.keywords: IUIAutomationVirtualizedItemPattern interface [Windows Accessibility],Realize method, IUIAutomationVirtualizedItemPattern.Realize, IUIAutomationVirtualizedItemPattern::Realize, Realize, Realize method [Windows Accessibility], Realize method [Windows Accessibility],IUIAutomationVirtualizedItemPattern interface, uiauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize, uiauto_IUIAutomationVirtualizedItemPattern_Realize, uiautomationclient/IUIAutomationVirtualizedItemPattern::Realize, winauto.uiauto_IUIAutomationVirtualizedItemPattern_Realize
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
 - IUIAutomationVirtualizedItemPattern::Realize
 - uiautomationclient/IUIAutomationVirtualizedItemPattern::Realize
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
 - IUIAutomationVirtualizedItemPattern.Realize
---

# IUIAutomationVirtualizedItemPattern::Realize


## -description

Creates a full UI Automation element for a virtualized item.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A virtualized item is represented by a placeholder automation element in the UI Automation tree. The <b>Realize</b> method causes the provider to make full information available for the item so that a full UI Automation element can be created for the item.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationvirtualizeditempattern">IUIAutomationVirtualizedItemPattern</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-workingwithvirtualizeditems">Working with Virtualized Items</a>
