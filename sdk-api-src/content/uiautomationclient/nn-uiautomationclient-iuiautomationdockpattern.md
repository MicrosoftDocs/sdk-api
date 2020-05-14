---
UID: NN:uiautomationclient.IUIAutomationDockPattern
title: IUIAutomationDockPattern (uiautomationclient.h)
description: Provides access to a control that enables child elements to be arranged horizontally and vertically, relative to each other.helpviewer_keywords: ["IUIAutomationDockPattern","IUIAutomationDockPattern interface [Windows Accessibility]","IUIAutomationDockPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationDockPattern","uiauto_IUIAutomationDockPattern","uiautomationclient/IUIAutomationDockPattern","winauto.uiauto_IUIAutomationDockPattern"]
old-location: winauto\uiauto_IUIAutomationDockPattern.htm
tech.root: WinAuto
ms.assetid: 2da816f0-9674-4b48-bb82-4eba941a7fa4
ms.date: 12/05/2018
ms.keywords: IUIAutomationDockPattern, IUIAutomationDockPattern interface [Windows Accessibility], IUIAutomationDockPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationDockPattern, uiauto_IUIAutomationDockPattern, uiautomationclient/IUIAutomationDockPattern, winauto.uiauto_IUIAutomationDockPattern
f1_keywords:
- uiautomationclient/IUIAutomationDockPattern
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
- IUIAutomationDockPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationDockPattern interface


## -description


Provides access to  a control that enables child elements to be arranged horizontally and vertically, relative to each other.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationDockPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationDockPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationDockPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition">SetDockPosition</a>
</td>
<td align="left" width="63%">
Sets the dock position of this element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationDockPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition">CachedDockPosition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached dock position of this element within its docking container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdockpattern-get_currentdockposition">CurrentDockPosition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the dock position of this element within its docking container.

</td>
</tr>
</table> 


## -remarks



Microsoft UI Automation client applications use this interface to access the dock properties of UI Automation elements that function as controls within a docking container. A docking container is a control that allows the arrangement of child elements, both horizontally and vertically, relative to the boundaries of the docking container and other elements within the container. Controls are docked relative to each other based on their current z-order; the higher their z-order placement the farther they are placed from the specified edge of the docking container.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

