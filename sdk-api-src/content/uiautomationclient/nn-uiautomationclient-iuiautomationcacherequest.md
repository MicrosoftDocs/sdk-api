---
UID: NN:uiautomationclient.IUIAutomationCacheRequest
title: IUIAutomationCacheRequest
author: windows-sdk-content
description: Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.
old-location: winauto\uiauto_IUIAutomationCacheRequest.htm
old-project: WinAuto
ms.assetid: 8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUIAutomationCacheRequest, IUIAutomationCacheRequest interface [Windows Accessibility], IUIAutomationCacheRequest interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationCacheRequest, uiauto_IUIAutomationCacheRequest, uiautomationclient/IUIAutomationCacheRequest, winauto.uiauto_IUIAutomationCacheRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationCacheRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationCacheRequest interface


## -description


Exposes properties and methods of a cache request. Client applications use this interface to specify the properties and control patterns to be cached when a Microsoft UI Automation element is obtained.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationCacheRequest</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationCacheRequest</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f081d4da-2fba-4846-813c-33e11c09315b">AddPattern</a>
</td>
<td align="left" width="63%">
Adds a control pattern to the cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61e56133-fb9e-4556-a9be-f7270b1d2bfb">AddProperty</a>
</td>
<td align="left" width="63%">
Adds a property to the cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
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

<a href="https://msdn.microsoft.com/dd4c6407-d14e-4e67-9681-1f90741da38e">AutomationElementMode</a>


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

<a href="https://msdn.microsoft.com/da9c9c9a-7ada-4f72-a025-1202e500241d">TreeFilter</a>


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

<a href="https://msdn.microsoft.com/3e45f35c-8a24-482f-acb6-9af6ce05d7fd">TreeScope</a>


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

Create a new cache request by calling <a href="https://msdn.microsoft.com/e61aecac-8c08-4f83-b3e6-f4baedcb16c6">CreateCacheRequest</a>, and configure the request by calling methods of <b>IUIAutomationCacheRequest</b>.




## -see-also




<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

