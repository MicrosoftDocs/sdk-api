---
UID: NN:uiautomationcore.IDockProvider
title: IDockProvider
author: windows-sdk-content
description: Provides access to an element in a docking container.
old-location: winauto\uiauto_IDockProvider.htm
tech.root: WinAuto
ms.assetid: 106ca4b4-1304-4942-88a4-79a3895b552f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IDockProvider, IDockProvider interface [Windows Accessibility], IDockProvider interface [Windows Accessibility],described, uiauto.uiauto_IDockProvider, uiauto_IDockProvider, uiautomationcore/IDockProvider, winauto.uiauto_IDockProvider
ms.prod: windows
ms.technology: windows-sdk
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
 - IDockProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockProvider interface


## -description


Provides access 
        to an element in a docking container.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDockProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDockProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e3d9a59-6bf4-4980-b318-f1badb0f8031">SetDockPosition</a>
</td>
<td align="left" width="63%">
Sets the docking position of this element. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa170dec-a4e1-48ac-8434-a24b79006653">DockPosition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates the current docking position of this element.
				

</td>
</tr>
</table> 


## -remarks



<b>IDockProvider</b> does not expose any properties of the docking 
        container or any properties of controls that might be docked adjacent to the current 
        control in the docking container.
        

Controls are docked relative to each other based on their current z-order; 
        the higher their z-order placement, the farther they are placed from the specified edge of the docking container.
        




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a6ea269b-632e-48ce-ac3b-edd7cc34d986">Dock Control Pattern</a>



<a href="https://msdn.microsoft.com/36ed98c2-f111-4192-8ce2-b8dd7da47de5">DockPosition</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

