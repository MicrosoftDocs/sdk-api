---
UID: NN:wbemdisp.ISWbemRefresher
title: ISWbemRefresher
author: windows-sdk-content
description: The SWbemRefresher object is a container object that can refresh the data for all the objects added to it. The set of added objects, each item represented by an SWbemRefreshableItem instance can be treated as a collection and enumerated.
old-location: wmi\swbemrefresher.htm
old-project: WmiSdk
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemRefresher, SWbemRefresher, SWbemRefresher object [Windows Management Instrumentation], SWbemRefresher object [Windows Management Instrumentation],described, _hmm_swbemrefresher, wbemdisp/SWbemRefresher, wmi.swbemrefresher
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemRefresher
 - ISWbemRefresher
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemRefresher interface


## -description


The 
<b>SWbemRefresher</b> object is a container object that can refresh the data for all the objects that are added to it. Single instances and instance enumerators can be added or removed from the container. The set of added objects, each item represented by an 
<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a> instance, can be treated as a collection and enumerated. WMI instances from any class can be added to the 
<b>SWbemRefresher</b> object. Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the 
<a href="https://msdn.microsoft.com/85a4777a-4be7-44f2-b7a6-e18b5e57f7af">Refresh</a> call. If the data is supplied through a high-performance provider and the 
<a href="https://msdn.microsoft.com/3be24128-8a35-44b0-befd-8b8937eff1b7">AutoReconnect</a> property is <b>TRUE</b>, then the 
<b>SWbemRefresher</b> object attempts to reestablish a broken connection to the data provider. This object can be created by the VBScript <b>CreateObject </b>call.

The refresh operation can be carried out by calling either the 
<a href="https://msdn.microsoft.com/85a4777a-4be7-44f2-b7a6-e18b5e57f7af">SWbemRefresher.Refresh</a> method or 
the <a href="https://msdn.microsoft.com/6aeaa336-fb98-4eda-b746-fc958198d8ae">SWbemObjectEx.Refresh_</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemRefresher</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemRefresher</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a new refreshable object to the collection in the refresher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406603">AddEnum</a>
</td>
<td align="left" width="63%">
Adds a new enumerator to the refresher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6e462d3-52b3-40c0-9a9c-fa268415a5f0">DeleteAll</a>
</td>
<td align="left" width="63%">
Removes all items from the collection in the refresher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Returns a specified refresher item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85a4777a-4be7-44f2-b7a6-e18b5e57f7af">Refresh</a>
</td>
<td align="left" width="63%">
Updates all the items that are contained in the refresher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes the refresher item object or object set with a specified index from the refresher.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemRefresher</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3be24128-8a35-44b0-befd-8b8937eff1b7">AutoReconnect</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the number of items in the refresher object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/944d4cdc-ad35-4b53-b755-f10131a087fb">SWbemObjectEx</a>



<a href="https://msdn.microsoft.com/6a12c8eb-3ef9-4292-810c-6954294fc8c7">SWbemRefreshableItem</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

