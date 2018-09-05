---
UID: NF:uiautomationcore.ISelectionItemProvider.RemoveFromSelection
title: ISelectionItemProvider::RemoveFromSelection
author: windows-sdk-content
description: Removes the current element from the collection of selected items.
old-location: winauto\uiauto_ISelectionItemProvider_RemoveFromSelection.htm
old-project: WinAuto
ms.assetid: fcbf452e-5827-4368-b601-a6eeabb15d53
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISelectionItemProvider interface [Windows Accessibility],RemoveFromSelection method, ISelectionItemProvider.RemoveFromSelection, ISelectionItemProvider::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],ISelectionItemProvider interface, uiauto.uiauto_ISelectionItemProvider_RemoveFromSelection, uiauto_ISelectionItemProvider_RemoveFromSelection, uiautomationcore/ISelectionItemProvider::RemoveFromSelection, winauto.uiauto_ISelectionItemProvider_RemoveFromSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISelectionItemProvider.RemoveFromSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISelectionItemProvider::RemoveFromSelection


## -description


Removes the current element from the collection of selected items.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Send an <a href="uiauto_event_ids.htm">UIA_SelectionItem_ElementRemovedFromSelectionEventId</a> event as appropriate. 

<div class="alert"><b>Note</b>  This rule does not depend on whether the container allows single or multiple selection, 
			or on what method was used to change the selection. Only the result matters.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/464b05e3-06da-44b9-b4a6-c64452fcdb6d">ISelectionItemProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

