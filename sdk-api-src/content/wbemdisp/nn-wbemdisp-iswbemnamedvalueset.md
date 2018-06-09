---
UID: NN:wbemdisp.ISWbemNamedValueSet
title: ISWbemNamedValueSet
author: windows-sdk-content
description: An SWbemNamedValueSet object is a collection of SWbemNamedValue objects.
old-location: wmi\swbemnamedvalueset.htm
old-project: WmiSdk
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemNamedValueSet, SWbemNamedValueSet, SWbemNamedValueSet object [Windows Management Instrumentation], SWbemNamedValueSet object [Windows Management Instrumentation],described, _hmm_swbemnamedvalueset, wbemdisp/SWbemNamedValueSet, wmi.swbemnamedvalueset
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
 - SWbemNamedValueSet
 - ISWbemNamedValueSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemNamedValueSet interface


## -description


An 
<b>SWbemNamedValueSet</b> object is a collection of 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> objects. The methods and properties of 
<b>SWbemNamedValueSet</b> are used principally to send more information to providers when submitting certain calls to WMI. All calls in 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>, and some calls in 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, take an optional parameter that is an object of this type. A client can add information to an 
<b>SWbemNamedValueSet</b> object, and send the 
<b>SWbemNamedValueSet</b> object with the call as one of the parameters. This object can be created by the VBScript <b>CreateObject</b> call.

For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.
<div class="alert"><b>Note</b>  Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI. If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible. If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information. This mechanism allows you to access such providers, if necessary.</div><div> </div>An 
<b>SWbemNamedValueSet</b> object is a collection of 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> elements. These items are added to the collection using the 
<a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method. They are removed using the 
<a href="https://msdn.microsoft.com/8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4">SWbemNamedValueSet.Remove</a> method and retrieved using the 
<a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. You can access the methods to fill in any context information that is required by a dynamic provider. After you call one of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> methods, you can reuse the 
<b>SWbemNamedValueSet</b> object for another call.

The underlying provider determines the information that is contained in an 
<b>SWbemNamedValueSet</b> object. WMI makes no use of the information, but simply forwards it to the provider. Providers must publish the context information they require to service requests.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemNamedValueSet</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemNamedValueSet</b> object has these methods.
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
Adds an 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of this 
<b>SWbemNamedValueSet</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db5d2e68-028e-4902-ad42-0b46e1a96bcb">DeleteAll</a>
</td>
<td align="left" width="63%">
Removes all items from the collection, making the 
<b>SWbemNamedValueSet</b>
     object empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object from the collection. This is the default method of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemNamedValueSet</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of items in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

