---
UID: NN:uiautomationclient.IUIAutomationProxyFactoryEntry
title: IUIAutomationProxyFactoryEntry (uiautomationclient.h)
description: Represents a proxy factory in the table maintained by Microsoft UI Automation, and exposes properties and methods that can be used by client applications to interact with IUIAutomationProxyFactory objects.
old-location: winauto\uiauto_IUIAutomationProxyFactoryEntry.htm
tech.root: WinAuto
ms.assetid: 0507deef-35dc-45bb-a7c1-82b84344ee17
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryEntry, IUIAutomationProxyFactoryEntry interface [Windows Accessibility], IUIAutomationProxyFactoryEntry interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationProxyFactoryEntry, uiauto_IUIAutomationProxyFactoryEntry, uiautomationclient/IUIAutomationProxyFactoryEntry, winauto.uiauto_IUIAutomationProxyFactoryEntry
f1_keywords:
- uiautomationclient/IUIAutomationProxyFactoryEntry
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
- IUIAutomationProxyFactoryEntry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationProxyFactoryEntry interface


## -description


Represents a proxy factory in the table maintained by Microsoft UI Automation, and exposes properties and methods that can be used by client applications to interact with <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactory">IUIAutomationProxyFactory</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryEntry</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationProxyFactoryEntry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationProxyFactoryEntry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-getwineventsforautomationevent">GetWinEventsForAutomationEvent</a>
</td>
<td align="left" width="63%">
Retrieves the list of WinEvents that are mapped to a specific UI Automation event. If an element represented by this proxy raises one the listed WinEvents, the proxy handles it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-setwineventsforautomationevent">SetWinEventsForAutomationEvent</a>
</td>
<td align="left" width="63%">
Maps UI Automation events to WinEvents.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryEntry</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_allowsubstringmatch">AllowSubstringMatch</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the proxy allows substring matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_cancheckbaseclass">CanCheckBaseClass</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the base class can be checked when searching for a proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_classname">ClassName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the window class served by the proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_imagename">ImageName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the image of the proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_needsadviseevents">NeedsAdviseEvents</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the proxy must be notified when an application has registered for events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-get_proxyfactory">ProxyFactory</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the proxy factory associated with this entry.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-proxyfactoryinterfaces">Proxy Factory Interfaces for Clients</a>
 

 

