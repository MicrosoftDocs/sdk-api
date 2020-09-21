---
UID: NN:uiautomationclient.IUIAutomationCacheRequest
title: IUIAutomationCacheRequest (uiautomationclient.h)
description: Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.
helpviewer_keywords: ["IUIAutomationCacheRequest","IUIAutomationCacheRequest interface [Windows Accessibility]","IUIAutomationCacheRequest interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationCacheRequest","uiauto_IUIAutomationCacheRequest","uiautomationclient/IUIAutomationCacheRequest","winauto.uiauto_IUIAutomationCacheRequest"]
old-location: winauto\uiauto_IUIAutomationCacheRequest.htm
tech.root: WinAuto
ms.assetid: 8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41
ms.date: 12/05/2018
ms.keywords: IUIAutomationCacheRequest, IUIAutomationCacheRequest interface [Windows Accessibility], IUIAutomationCacheRequest interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationCacheRequest, uiauto_IUIAutomationCacheRequest, uiautomationclient/IUIAutomationCacheRequest, winauto.uiauto_IUIAutomationCacheRequest
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
 - IUIAutomationCacheRequest
 - uiautomationclient/IUIAutomationCacheRequest
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
 - IUIAutomationCacheRequest
---

# IUIAutomationCacheRequest interface


## -description

Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationCacheRequest</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationCacheRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationCacheRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-addpattern">AddPattern</a>
</td>
<td align="left" width="63%">
Adds a control pattern to the cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-addproperty">AddProperty</a>
</td>
<td align="left" width="63%">
Adds a property to the cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the cache request.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationCacheRequest</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode">AutomationElementMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether returned elements contain full references to the underlying UI, or only cached information. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter">TreeFilter</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the view of the UI Automation element tree that is used when caching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope">TreeScope</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the scope of caching.

</td>
</tr>
</table>

## -remarks

Retrieving properties and control patterns through UI Automation requires cross-process calls that can slow down performance. By caching values of proprieties and control patterns in a batch operation, you can enhance the performance of your application.

Create a new cache request by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createcacherequest">CreateCacheRequest</a>, and configure the request by calling methods of <b>IUIAutomationCacheRequest</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>