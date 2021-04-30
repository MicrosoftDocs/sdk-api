---
UID: NN:uiautomationcore.ISelectionProvider2
title: ISelectionProvider2 (uiautomationcore.h)
description: Extends the ISelectionItemProvider interface to provide information about selected items.
helpviewer_keywords: ["ISelectionProvider2","ISelectionProvider2 interface [Windows Accessibility]","ISelectionProvider2 interface [Windows Accessibility]","described","uiautomationcore/ISelectionProvider2","winauto.uiauto_ISelectionProvider2"]
old-location: winauto\uiauto_ISelectionProvider2.htm
tech.root: WinAuto
ms.assetid: 1FC0406D-6924-4C24-8491-E18BA33DAFEB
ms.date: 12/05/2018
ms.keywords: ISelectionProvider2, ISelectionProvider2 interface [Windows Accessibility], ISelectionProvider2 interface [Windows Accessibility],described, uiautomationcore/ISelectionProvider2, winauto.uiauto_ISelectionProvider2
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISelectionProvider2
 - uiautomationcore/ISelectionProvider2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ISelectionProvider2
---

# ISelectionProvider2 interface


## -description

Extends the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a> interface to provide information about selected items.

## -remarks

This interface is implemented by a Microsoft UI Automation provider.

Providers should raise an event of type <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_Selection_InvalidatedEventId</a> when a selection in a container has changed significantly.


When selecting from a list or 2D grid there are primary pieces of information that ATs would like to better read to their end users.  Using Excel as a primary example, there are 4 main pieces of information necessary for the AT to provide a good experience:  

<ul>
<li>The first cell in the selection</li>
<li>The last cell in the selection</li>
<li>The current item as you select</li>
<li>The total count</li>
</ul>
<img alt="Image of an Excel spreadsheet showing multiple cells selected. Selection starts in the upper right on cell F5 and ends in the lower left on cell D7." src="./images/ISelectionPattern2.png"/>
The above image illustrates the end state of a 2D selection:


<ul>
<li>The user started in cell F5 (note this is where focus input stays because if you type that is where data lands)</li>
<li>The user selects down the column to cell F7</li>
<li>The user then selects left to cell D7</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>