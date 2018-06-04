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

# IWSMan interface


## -description


Provides methods and properties used to create a session, represented by a <a href="https://msdn.microsoft.com/b98ca759-71cb-492e-8645-8766b202eb36">Session</a> object. Any Windows Remote Management operations require creation of a <a href="https://msdn.microsoft.com/b98ca759-71cb-492e-8645-8766b202eb36">Session</a> that connects to a remote computer, <a href="windows_remote_management_glossary.htm">base management controller</a> (BMC), or the local computer. Operations include getting, writing, or enumerating data, or invoking methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSMan</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSMan</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWSMan</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateConnectionOptions</b></td>
<td align="left" width="63%">
Creates a,  <a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a> object that specifies the user name and password  used when  creating a remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateSession</b></td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object that can then be used for subsequent network operations.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSMan</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>CommandLine</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the unprocessed command line for the current hosting process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Error</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets error information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/45895a4e-b7de-4469-ae78-6d1d3f9d6145">WSMan</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

