---
UID: NN:uiautomationclient.IUIAutomationTogglePattern
title: IUIAutomationTogglePattern (uiautomationclient.h)
description: Provides access to a control that can cycle through a set of states, and maintain a state after it is set.
helpviewer_keywords: ["IUIAutomationTogglePattern","IUIAutomationTogglePattern interface [Windows Accessibility]","IUIAutomationTogglePattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTogglePattern","uiauto_IUIAutomationTogglePattern","uiautomationclient/IUIAutomationTogglePattern","winauto.uiauto_IUIAutomationTogglePattern"]
old-location: winauto\uiauto_IUIAutomationTogglePattern.htm
tech.root: WinAuto
ms.assetid: f2e69387-271f-4f85-85d5-19ba5d231f85
ms.date: 12/05/2018
ms.keywords: IUIAutomationTogglePattern, IUIAutomationTogglePattern interface [Windows Accessibility], IUIAutomationTogglePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTogglePattern, uiauto_IUIAutomationTogglePattern, uiautomationclient/IUIAutomationTogglePattern, winauto.uiauto_IUIAutomationTogglePattern
f1_keywords:
- uiautomationclient/IUIAutomationTogglePattern
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
- IUIAutomationTogglePattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTogglePattern interface


## -description


Provides access to a control that can cycle through a set of states, and maintain a state after it is set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTogglePattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTogglePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTogglePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtogglepattern-toggle">Toggle</a>
</td>
<td align="left" width="63%">
Cycles through the toggle states of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTogglePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtogglepattern-get_cachedtogglestate">CachedToggleState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached state of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate">CurrentToggleState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the state of the control.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

