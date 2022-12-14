---
UID: NF:uiautomationclient.IUIAutomationDragPattern.GetCachedGrabbedItems
title: IUIAutomationDragPattern::GetCachedGrabbedItems (uiautomationclient.h)
description: Retrieves a cached collection of elements that represent the full set of items that the user is dragging as part of a drag operation.
helpviewer_keywords: ["GetCachedGrabbedItems","GetCachedGrabbedItems method [Windows Accessibility]","GetCachedGrabbedItems method [Windows Accessibility]","IUIAutomationDragPattern interface","IUIAutomationDragPattern interface [Windows Accessibility]","GetCachedGrabbedItems method","IUIAutomationDragPattern.GetCachedGrabbedItems","IUIAutomationDragPattern::GetCachedGrabbedItems","uiautomationclient/IUIAutomationDragPattern::GetCachedGrabbedItems","winauto.uiauto_iuiautomationdragpattern_getcachedgrabbeditems"]
old-location: winauto\uiauto_iuiautomationdragpattern_getcachedgrabbeditems.htm
tech.root: WinAuto
ms.assetid: A3CB19E9-634D-4023-926E-BAA717DE4528
ms.date: 12/05/2018
ms.keywords: GetCachedGrabbedItems, GetCachedGrabbedItems method [Windows Accessibility], GetCachedGrabbedItems method [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],GetCachedGrabbedItems method, IUIAutomationDragPattern.GetCachedGrabbedItems, IUIAutomationDragPattern::GetCachedGrabbedItems, uiautomationclient/IUIAutomationDragPattern::GetCachedGrabbedItems, winauto.uiauto_iuiautomationdragpattern_getcachedgrabbeditems
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationDragPattern::GetCachedGrabbedItems
 - uiautomationclient/IUIAutomationDragPattern::GetCachedGrabbedItems
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
 - IUIAutomationDragPattern.GetCachedGrabbedItems
---

# IUIAutomationDragPattern::GetCachedGrabbedItems


## -description

Retrieves a cached collection of elements that represent the full set of items that the user is dragging as part of a drag operation.

## -parameters

### -param retVal [out, retval, optional]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IAutomationElementArray</a>**</b>

The cached collection of elements that the user is dragging. This property is <b>NULL</b> or an empty array if only a single item is being dragged. The default value is an empty array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the user is dragging multiple items, the items are represented by a single master element with an associated set of grabbed elements.  The master item fires the appropriate events, to avoid having a large set of duplicate events.  The client can query the GrabbedItems property to get the full list of grabbed items.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdragpattern">IUIAutomationDragPattern</a>