---
UID: NN:uiautomationcore.ISelectionItemProvider
title: ISelectionItemProvider
author: windows-driver-content
description: Provides access to individual, selectable child controls of containers that implement ISelectionProvider.
old-location: winauto\uiauto_ISelectionItemProvider.htm
old-project: WinAuto
ms.assetid: 464b05e3-06da-44b9-b4a6-c64452fcdb6d
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: ISelectionItemProvider, ISelectionItemProvider interface [Windows Accessibility], ISelectionItemProvider interface [Windows Accessibility], described, uiauto.uiauto_ISelectionItemProvider, uiauto_ISelectionItemProvider, uiautomationcore/ISelectionItemProvider, winauto.uiauto_ISelectionItemProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	ISelectionItemProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISelectionItemProvider interface


## -description


Provides 
        access to individual, selectable child controls of containers that implement 
        <a href="https://msdn.microsoft.com/e02731f8-e58d-4c66-95bf-005cf954471c">ISelectionProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionItemProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISelectionItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISelectionItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c54d57f-7cca-4068-80d9-995c46de1962">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the current element to the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcbf452e-5827-4368-b601-a6eeabb15d53">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes the current element from the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b11e3472-e7dc-462d-93f4-e02f07ebd45f">Select</a>
</td>
<td align="left" width="63%">
Deselects any selected items and then selects the current element. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionItemProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/15172a66-385a-437e-8f79-a696708971e3">IsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether an item is selected. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c1bfdb40-f30c-4f33-a947-875077000029">SelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the provider that implements <a href="https://msdn.microsoft.com/e02731f8-e58d-4c66-95bf-005cf954471c">ISelectionProvider</a> 
        and acts as the container for the calling object.
        

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that 
            must support the <a href="https://msdn.microsoft.com/9314547f-7062-42db-b6a7-8a8eaef21d4e">SelectionItem</a> control pattern.




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

