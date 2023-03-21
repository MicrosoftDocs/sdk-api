---
UID: NF:uiautomationcore.ISelectionItemProvider.AddToSelection
title: ISelectionItemProvider::AddToSelection (uiautomationcore.h)
description: Adds the current element to the collection of selected items. (ISelectionItemProvider.AddToSelection)
helpviewer_keywords: ["AddToSelection","AddToSelection method [Windows Accessibility]","AddToSelection method [Windows Accessibility]","ISelectionItemProvider interface","ISelectionItemProvider interface [Windows Accessibility]","AddToSelection method","ISelectionItemProvider.AddToSelection","ISelectionItemProvider::AddToSelection","uiauto.uiauto_ISelectionItemProvider_AddToSelection","uiauto_ISelectionItemProvider_AddToSelection","uiautomationcore/ISelectionItemProvider::AddToSelection","winauto.uiauto_ISelectionItemProvider_AddToSelection"]
old-location: winauto\uiauto_ISelectionItemProvider_AddToSelection.htm
tech.root: WinAuto
ms.assetid: 7c54d57f-7cca-4068-80d9-995c46de1962
ms.date: 12/05/2018
ms.keywords: AddToSelection, AddToSelection method [Windows Accessibility], AddToSelection method [Windows Accessibility],ISelectionItemProvider interface, ISelectionItemProvider interface [Windows Accessibility],AddToSelection method, ISelectionItemProvider.AddToSelection, ISelectionItemProvider::AddToSelection, uiauto.uiauto_ISelectionItemProvider_AddToSelection, uiauto_ISelectionItemProvider_AddToSelection, uiautomationcore/ISelectionItemProvider::AddToSelection, winauto.uiauto_ISelectionItemProvider_AddToSelection
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ISelectionItemProvider::AddToSelection
 - uiautomationcore/ISelectionItemProvider::AddToSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISelectionItemProvider.AddToSelection
---

# ISelectionItemProvider::AddToSelection


## -description

Adds the current element to the collection of selected items.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the result of a call to <b>ISelectionItemProvider::AddToSelection</b> is that a single item is selected, then 
			send an <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_SelectionItem_ElementSelectedEventId</a> event for that element; otherwise send an <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_SelectionItem_ElementAddedToSelectionEventId</a> or 
			<a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_SelectionItem_ElementRemovedFromSelectionEventId</a> event as appropriate. 

<div class="alert"><b>Note</b>  This rule does not depend on whether the container allows single or multiple selection, 
			or on what method was used to change the selection. Only the result matters.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
