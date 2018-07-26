---
UID: NN:uiautomationcore.IToggleProvider
title: IToggleProvider
author: windows-sdk-content
description: Provides access to controls that can cycle through a set of states and maintain a state after it is set.
old-location: winauto\uiauto_IToggleProvider.htm
old-project: WinAuto
ms.assetid: 85da8225-31b8-4b4d-81f4-ad98871b8e31
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IToggleProvider, IToggleProvider interface [Windows Accessibility], IToggleProvider interface [Windows Accessibility],described, uiauto.uiauto_IToggleProvider, uiauto_IToggleProvider, uiautomationcore/IToggleProvider, winauto.uiauto_IToggleProvider
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IToggleProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IToggleProvider interface


## -description


Provides access to 
        controls that can cycle through a set of states and maintain a state after it is set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToggleProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IToggleProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IToggleProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afadbcaf-156f-496e-a0f3-900e7f8d44da">Toggle</a>
</td>
<td align="left" width="63%">

        Cycles through the toggle states of a control.
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToggleProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/57bd9b77-32f4-4abf-b942-c0fe00398e56">ToggleState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The toggle state of the control.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/9fd1232b-199a-41e6-81b0-667c7e463d09">Toggle</a> control pattern.
			




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

