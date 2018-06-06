---
UID: NF:uiautomationclient.IUIAutomationDragPattern.GetCurrentGrabbedItems
title: IUIAutomationDragPattern::GetCurrentGrabbedItems
author: windows-sdk-content
description: Retrieves a collection of elements that represent the full set of items that the user is dragging as part of a drag operation.
old-location: winauto\uiauto_iuiautomationdragpattern_getcurrentgrabbeditems.htm
old-project: WinAuto
ms.assetid: 9311E1E3-FE4E-428F-9DAD-32AE347477EF
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetCurrentGrabbedItems, GetCurrentGrabbedItems method [Windows Accessibility], GetCurrentGrabbedItems method [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],GetCurrentGrabbedItems method, IUIAutomationDragPattern.GetCurrentGrabbedItems, IUIAutomationDragPattern::GetCurrentGrabbedItems, uiautomationclient/IUIAutomationDragPattern::GetCurrentGrabbedItems, winauto.uiauto_iuiautomationdragpattern_getcurrentgrabbeditems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationDragPattern.GetCurrentGrabbedItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationDragPattern::GetCurrentGrabbedItems


## -description


Retrieves a collection of elements that represent the full set of items that the user is dragging as part of a drag operation.  


## -parameters




### -param retVal [out, retval, optional]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IAutomationElementArray</a>**</b>

The collection of elements that the user is dragging. This property is <b>NULL</b> or an empty array if only a single item is being dragged. The default value is an empty array. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the user is dragging multiple items, the items are represented by a single master element with an associated set of grabbed elements.  The master item fires the appropriate events, to avoid having a large set of duplicate events.  The client can query the GrabbedItems property to get the full list of grabbed items.  




## -see-also




<a href="https://msdn.microsoft.com/F7768A87-3981-48E0-A72D-BEA14C189E6E">IUIAutomationDragPattern</a>
 

 

