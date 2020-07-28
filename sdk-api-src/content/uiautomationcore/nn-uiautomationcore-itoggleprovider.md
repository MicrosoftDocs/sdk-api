---
UID: NN:uiautomationcore.IToggleProvider
title: IToggleProvider (uiautomationcore.h)
description: Provides access to controls that can cycle through a set of states and maintain a state after it is set.
helpviewer_keywords: ["IToggleProvider","IToggleProvider interface [Windows Accessibility]","IToggleProvider interface [Windows Accessibility]","described","uiauto.uiauto_IToggleProvider","uiauto_IToggleProvider","uiautomationcore/IToggleProvider","winauto.uiauto_IToggleProvider"]
old-location: winauto\uiauto_IToggleProvider.htm
tech.root: WinAuto
ms.assetid: 85da8225-31b8-4b4d-81f4-ad98871b8e31
ms.date: 12/05/2018
ms.keywords: IToggleProvider, IToggleProvider interface [Windows Accessibility], IToggleProvider interface [Windows Accessibility],described, uiauto.uiauto_IToggleProvider, uiauto_IToggleProvider, uiautomationcore/IToggleProvider, winauto.uiauto_IToggleProvider
f1_keywords:
- uiautomationcore/IToggleProvider
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
- IToggleProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IToggleProvider interface


## -description


Provides access to 
        controls that can cycle through a set of states and maintain a state after it is set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToggleProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IToggleProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itoggleprovider-toggle">Toggle</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itoggleprovider-get_togglestate">ToggleState</a>


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



Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingtoggle">Toggle</a> control pattern.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

