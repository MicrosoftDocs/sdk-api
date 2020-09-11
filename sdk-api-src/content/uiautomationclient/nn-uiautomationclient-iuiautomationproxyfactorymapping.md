---
UID: NN:uiautomationclient.IUIAutomationProxyFactoryMapping
title: IUIAutomationProxyFactoryMapping (uiautomationclient.h)
description: Exposes properties and methods for a table of proxy factories. Each table entry is represented by an IUIAutomationProxyFactoryEntry interface. The entries are in the order in which the system will attempt to use the proxies.
helpviewer_keywords: ["IUIAutomationProxyFactoryMapping","IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","IUIAutomationProxyFactoryMapping interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationProxyFactoryMapping","uiauto_IUIAutomationProxyFactoryMapping","uiautomationclient/IUIAutomationProxyFactoryMapping","winauto.uiauto_IUIAutomationProxyFactoryMapping"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping.htm
tech.root: WinAuto
ms.assetid: 7a938c1c-a11c-4fdd-a73a-e7656032f21e
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryMapping, IUIAutomationProxyFactoryMapping interface [Windows Accessibility], IUIAutomationProxyFactoryMapping interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationProxyFactoryMapping, uiauto_IUIAutomationProxyFactoryMapping, uiautomationclient/IUIAutomationProxyFactoryMapping, winauto.uiauto_IUIAutomationProxyFactoryMapping
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationProxyFactoryMapping
 - uiautomationclient/IUIAutomationProxyFactoryMapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationProxyFactoryMapping
---

# IUIAutomationProxyFactoryMapping interface


## -description

Exposes properties and methods for a table of proxy factories. Each table entry is represented by an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a> interface. The entries are in the order in which the system will attempt to use the proxies.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryMapping</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationProxyFactoryMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationProxyFactoryMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-cleartable">ClearTable</a>
</td>
<td align="left" width="63%">
Removes all entries from the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-getentry">GetEntry</a>
</td>
<td align="left" width="63%">
Retrieves an entry from the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-gettable">GetTable</a>
</td>
<td align="left" width="63%">
Retrieves all entries in the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-insertentries">InsertEntries</a>
</td>
<td align="left" width="63%">
Inserts entries into the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-insertentry">InsertEntry</a>
</td>
<td align="left" width="63%">
Insert an entry into the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-removeentry">RemoveEntry</a>
</td>
<td align="left" width="63%">
Removes an entry from the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-restoredefaulttable">RestoreDefaultTable</a>
</td>
<td align="left" width="63%">
Restores the default table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-settable">SetTable</a>
</td>
<td align="left" width="63%">
Sets the table of proxy factories.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryMapping</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactorymapping-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of entries in the proxy factory table.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-proxyfactoryinterfaces">Proxy Factory Interfaces for Clients</a>

