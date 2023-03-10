---
UID: NF:uiautomationcore.ISelectionItemProvider.RemoveFromSelection
title: ISelectionItemProvider::RemoveFromSelection (uiautomationcore.h)
description: Removes the current element from the collection of selected items.
helpviewer_keywords: ["ISelectionItemProvider interface [Windows Accessibility]","RemoveFromSelection method","ISelectionItemProvider.RemoveFromSelection","ISelectionItemProvider::RemoveFromSelection","RemoveFromSelection","RemoveFromSelection method [Windows Accessibility]","RemoveFromSelection method [Windows Accessibility]","ISelectionItemProvider interface","uiauto.uiauto_ISelectionItemProvider_RemoveFromSelection","uiauto_ISelectionItemProvider_RemoveFromSelection","uiautomationcore/ISelectionItemProvider::RemoveFromSelection","winauto.uiauto_ISelectionItemProvider_RemoveFromSelection"]
old-location: winauto\uiauto_ISelectionItemProvider_RemoveFromSelection.htm
tech.root: WinAuto
ms.assetid: fcbf452e-5827-4368-b601-a6eeabb15d53
ms.date: 12/05/2018
ms.keywords: ISelectionItemProvider interface [Windows Accessibility],RemoveFromSelection method, ISelectionItemProvider.RemoveFromSelection, ISelectionItemProvider::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],ISelectionItemProvider interface, uiauto.uiauto_ISelectionItemProvider_RemoveFromSelection, uiauto_ISelectionItemProvider_RemoveFromSelection, uiautomationcore/ISelectionItemProvider::RemoveFromSelection, winauto.uiauto_ISelectionItemProvider_RemoveFromSelection
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
 - ISelectionItemProvider::RemoveFromSelection
 - uiautomationcore/ISelectionItemProvider::RemoveFromSelection
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
 - ISelectionItemProvider.RemoveFromSelection
---

# ISelectionItemProvider::RemoveFromSelection


## -description

Removes the current element from the collection of selected items.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Send an <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_SelectionItem_ElementRemovedFromSelectionEventId</a> event as appropriate. 

<div class="alert"><b>Note</b>  This rule does not depend on whether the container allows single or multiple selection, 
			or on what method was used to change the selection. Only the result matters.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
