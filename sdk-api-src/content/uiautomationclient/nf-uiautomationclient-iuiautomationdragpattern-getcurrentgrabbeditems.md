---
UID: NF:uiautomationclient.IUIAutomationDragPattern.GetCurrentGrabbedItems
title: IUIAutomationDragPattern::GetCurrentGrabbedItems (uiautomationclient.h)
description: Retrieves a collection of elements that represent the full set of items that the user is dragging as part of a drag operation.
helpviewer_keywords: ["GetCurrentGrabbedItems","GetCurrentGrabbedItems method [Windows Accessibility]","GetCurrentGrabbedItems method [Windows Accessibility]","IUIAutomationDragPattern interface","IUIAutomationDragPattern interface [Windows Accessibility]","GetCurrentGrabbedItems method","IUIAutomationDragPattern.GetCurrentGrabbedItems","IUIAutomationDragPattern::GetCurrentGrabbedItems","uiautomationclient/IUIAutomationDragPattern::GetCurrentGrabbedItems","winauto.uiauto_iuiautomationdragpattern_getcurrentgrabbeditems"]
old-location: winauto\uiauto_iuiautomationdragpattern_getcurrentgrabbeditems.htm
tech.root: WinAuto
ms.assetid: 9311E1E3-FE4E-428F-9DAD-32AE347477EF
ms.date: 12/05/2018
ms.keywords: GetCurrentGrabbedItems, GetCurrentGrabbedItems method [Windows Accessibility], GetCurrentGrabbedItems method [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],GetCurrentGrabbedItems method, IUIAutomationDragPattern.GetCurrentGrabbedItems, IUIAutomationDragPattern::GetCurrentGrabbedItems, uiautomationclient/IUIAutomationDragPattern::GetCurrentGrabbedItems, winauto.uiauto_iuiautomationdragpattern_getcurrentgrabbeditems
f1_keywords:
- uiautomationclient/IUIAutomationDragPattern.GetCurrentGrabbedItems
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IUIAutomationDragPattern.GetCurrentGrabbedItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationDragPattern::GetCurrentGrabbedItems


## -description


Retrieves a collection of elements that represent the full set of items that the user is dragging as part of a drag operation.  


## -parameters




### -param retVal [out, retval, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IAutomationElementArray</a>**</b>

The collection of elements that the user is dragging. This property is <b>NULL</b> or an empty array if only a single item is being dragged. The default value is an empty array. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the user is dragging multiple items, the items are represented by a single master element with an associated set of grabbed elements.  The master item fires the appropriate events, to avoid having a large set of duplicate events.  The client can query the GrabbedItems property to get the full list of grabbed items.  




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdragpattern">IUIAutomationDragPattern</a>
 

 

