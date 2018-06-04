---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMenuBand interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that allow a Component Object Model (COM) object to receive and translate appropriate messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuBand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMenuBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d30a456c-7c09-4250-8509-353c54d017b9">IsMenuMessage</a>
</td>
<td align="left" width="63%">
A message pump calls this method to see if any messages should be redirected to the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee1f64f-ca8b-4f50-bbab-24ff1216708c">TranslateMenuMessage</a>
</td>
<td align="left" width="63%">
Translates a message for a COM object.

</td>
</tr>
</table> 


## -remarks



 An application can call <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> with one of the following service IDs. If the <i>riid</i> parameter of <b>QueryService</b> is IAccessible or IDispatch, the call to <b>QueryService</b> creates a new accessibility object. Otherwise, the call to <b>QueryService</b> is equivalent to a call to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with the service ID, as follows:



<table class="clsStd">
<tr>
<th>Service ID (SID)</th>
<th>Meaning</th>
</tr>
<tr>
<td>SID_SMenuBandChild</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the submenu.</td>
</tr>
<tr>
<td>SID_SMenuBandParent</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the parent menu.</td>
</tr>
<tr>
<td>SID_SMenuBandTop</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the top menu.</td>
</tr>
</table>
 

In Windows 2000, this interface was implemented in browseui.dll. However, it is not recommended that this version be used.



