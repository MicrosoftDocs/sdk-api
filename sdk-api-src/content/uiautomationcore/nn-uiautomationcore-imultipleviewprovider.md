---
UID: NN:uiautomationcore.IMultipleViewProvider
title: IMultipleViewProvider (uiautomationcore.h)
author: windows-sdk-content
description: Provides access to controls that provide, and are able to switch between, multiple representations of the same set of information or child controls.
old-location: winauto\uiauto_IMultipleViewProvider.htm
tech.root: WinAuto
ms.assetid: 84d370a6-05bd-4efb-a6ca-99e9392f95dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMultipleViewProvider, IMultipleViewProvider interface [Windows Accessibility], IMultipleViewProvider interface [Windows Accessibility],described, uiauto.uiauto_IMultipleViewProvider, uiauto_IMultipleViewProvider, uiautomationcore/IMultipleViewProvider, winauto.uiauto_IMultipleViewProvider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IMultipleViewProvider"
dev_langs:
 - c++
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
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IMultipleViewProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultipleViewProvider interface


## -description


Provides access 
        to controls that provide, and are able to switch between, multiple representations of 
        the same set of information or child controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultipleViewProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultipleViewProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews">GetSupportedViews</a>
</td>
<td align="left" width="63%">
Retrieves a collection of control-specific view identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-getviewname">GetViewName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a control-specific view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-setcurrentview">SetCurrentView</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-imultipleviewprovider-get_currentview">CurrentView</a>


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
            <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingmultipleview">MultipleView</a> control pattern.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

