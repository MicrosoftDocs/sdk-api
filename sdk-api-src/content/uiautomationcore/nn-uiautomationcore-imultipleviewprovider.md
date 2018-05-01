---
UID: NN:uiautomationcore.IMultipleViewProvider
title: IMultipleViewProvider
author: windows-driver-content
description: Provides access to controls that provide, and are able to switch between, multiple representations of the same set of information or child controls.
old-location: winauto\uiauto_IMultipleViewProvider.htm
old-project: WinAuto
ms.assetid: 84d370a6-05bd-4efb-a6ca-99e9392f95dc
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IMultipleViewProvider, IMultipleViewProvider interface [Windows Accessibility], IMultipleViewProvider interface [Windows Accessibility], described, uiauto.uiauto_IMultipleViewProvider, uiauto_IMultipleViewProvider, uiautomationcore/IMultipleViewProvider, winauto.uiauto_IMultipleViewProvider
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
-	IMultipleViewProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMultipleViewProvider interface


## -description


Provides access 
        to controls that provide, and are able to switch between, multiple representations of 
        the same set of information or child controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultipleViewProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMultipleViewProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMultipleViewProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd4d5616-c126-455e-84e7-e62e24daf8f9">GetSupportedViews</a>
</td>
<td align="left" width="63%">
Retrieves a collection of control-specific view identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e9bca3-22cd-4f5b-9481-289bdfaf58e8">GetViewName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a control-specific view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfa652be-b6b6-44e3-b06a-8ead56f17d2d">SetCurrentView</a>
</td>
<td align="left" width="63%">
Sets the current control-specific view. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultipleViewProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9efc6d91-c922-4f03-9026-0dad454aad10">CurrentView</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Identifies the current view that the control is using to display information or child controls.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the 
            <a href="https://msdn.microsoft.com/c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed">MultipleView</a> control pattern.




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

