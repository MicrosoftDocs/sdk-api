---
UID: NN:uiautomationcore.IExpandCollapseProvider
title: IExpandCollapseProvider
author: windows-sdk-content
description: Provides access to a control that visually expands to display content, and collapses to hide content.
old-location: winauto\uiauto_IExpandCollapseProvider.htm
tech.root: WinAuto
ms.assetid: 59d91498-54f8-40df-8224-52ff8e45f6c3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IExpandCollapseProvider, IExpandCollapseProvider interface [Windows Accessibility], IExpandCollapseProvider interface [Windows Accessibility],described, uiauto.uiauto_IExpandCollapseProvider, uiauto_IExpandCollapseProvider, uiautomationcore/IExpandCollapseProvider, winauto.uiauto_IExpandCollapseProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IExpandCollapseProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExpandCollapseProvider interface


## -description


Provides 
        access to a control that visually expands to display content, and collapses to hide content.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExpandCollapseProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExpandCollapseProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IExpandCollapseProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4915a1b-9418-4601-9333-f9508d63079a">Collapse</a>
</td>
<td align="left" width="63%">
Hides all child nodes, controls, or content of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ac8c1fd-e754-439a-9bcf-92cb0974df91">Expand</a>
</td>
<td align="left" width="63%">
Displays all child nodes, controls, or content of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExpandCollapseProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0f0cdf30-97e5-45df-88a5-039e15e26420">ExpandCollapseState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates the state, expanded or collapsed, of the control.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/0ffc26c3-8696-44f9-b463-902a69e06d21">ExpandCollapse</a> control pattern.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9625a50d-b9fb-4f85-8245-c77cc53445c3">ExpandCollapseState</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

