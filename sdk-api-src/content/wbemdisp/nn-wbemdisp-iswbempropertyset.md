---
UID: NN:wbemdisp.ISWbemPropertySet
title: ISWbemPropertySet
author: windows-sdk-content
description: An SWbemPropertySet object is a collection of SWbemProperty objects.
old-location: wmi\swbempropertyset.htm
old-project: WmiSdk
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemPropertySet, SWbemPropertySet, SWbemPropertySet object [Windows Management Instrumentation], SWbemPropertySet object [Windows Management Instrumentation],described, _hmm_swbempropertyset, wbemdisp/SWbemPropertySet, wmi.swbempropertyset
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
 - SWbemPropertySet
 - ISWbemPropertySet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPropertySet interface


## -description


An 
<b>SWbemPropertySet</b> object is a collection of 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> objects. You can add items to the collection using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> method, retrieve items from the collection using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> method, and remove items from the collection using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a> method. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/3acbce31-6d56-4a7a-af03-fa37b2b868be">CreateObject</a> call.

The 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> objects that make up an 
<b>SWbemPropertySet</b> collection are used to describe the properties of a single WMI class or instance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemPropertySet</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemPropertySet</b> object has these methods.
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
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object to the 
<b>SWbemPropertySet</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Gets a named 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> from the collection. This is the default method for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Deletes an 
<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a> object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemPropertySet</b> object has these properties.
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
The number of items in the <b>SWbemPropertySet</b> collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

