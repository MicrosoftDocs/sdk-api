---
UID: NN:uiautomationcore.IExpandCollapseProvider
title: IExpandCollapseProvider (uiautomationcore.h)
author: windows-sdk-content
description: Provides access to a control that visually expands to display content, and collapses to hide content.
old-location: winauto\uiauto_IExpandCollapseProvider.htm
tech.root: WinAuto
ms.assetid: 59d91498-54f8-40df-8224-52ff8e45f6c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExpandCollapseProvider, IExpandCollapseProvider interface [Windows Accessibility], IExpandCollapseProvider interface [Windows Accessibility],described, uiauto.uiauto_IExpandCollapseProvider, uiauto_IExpandCollapseProvider, uiautomationcore/IExpandCollapseProvider, winauto.uiauto_IExpandCollapseProvider
ms.topic: interface
f1_keywords: ["uiautomationcore/IExpandCollapseProvider"]
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
ms.custom: 19H1
---

# IExpandCollapseProvider interface


## -description


Provides 
        access to a control that visually expands to display content, and collapses to hide content.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExpandCollapseProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExpandCollapseProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iexpandcollapseprovider-collapse">Collapse</a>
</td>
<td align="left" width="63%">
Hides all child nodes, controls, or content of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iexpandcollapseprovider-expand">Expand</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate">ExpandCollapseState</a>


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



Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingexpandcollapse">ExpandCollapse</a> control pattern.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-expandcollapsestate">ExpandCollapseState</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

