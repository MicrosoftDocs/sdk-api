---
UID: NN:certadm.IOCSPPropertyCollection
title: IOCSPPropertyCollection
author: windows-driver-content
description: Represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service.
old-location: security\iocsppropertycollection.htm
old-project: SecCrypto
ms.assetid: 8c700357-0cb4-4780-9ff1-ac57c46f9183
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCSPPropertyCollection, IOCSPPropertyCollection interface [Security], IOCSPPropertyCollection interface [Security], described, certadm/IOCSPPropertyCollection, security.iocsppropertycollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IOCSPPropertyCollection
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPPropertyCollection interface


## -description


The <b>IOCSPPropertyCollection</b> interface represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service. Microsoft provides a default implementation of this interface in the <b>OCSPPropertyCollection</b> class.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_OCSPPropertyCollection</b> class identifier.

In Visual Basic Scripting Edition, you create an instance of the <b>OCSPPropertyCollection</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOCSPPropertyCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IOCSPPropertyCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IOCSPPropertyCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e23a11-0550-47ae-9c24-90c1d18024a6">CreateProperty</a>
</td>
<td align="left" width="63%">
Creates a new property and adds it to a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f9a3e47-3757-42a9-bef2-93b8f304f618">DeleteProperty</a>
</td>
<td align="left" width="63%">
Removes a named property from a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46a20d55-a673-4f9b-9fb9-bfc631d70f99">GetAllProperties</a>
</td>
<td align="left" width="63%">
Gets all properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e944af4e-80e4-470e-be04-770cf0f89871">InitializeFromProperties</a>
</td>
<td align="left" width="63%">
Creates a property set from the properties contained in an existing server configuration.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOCSPPropertyCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Gets the number of properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Gets the property identified by index  in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0f7fe732-1d76-49c0-8b1e-a9950c85ca59">ItemByName</a>


</td>
<td align="left" width="63%">
Gets the property identified by name in a property set.

</td>
</tr>
</table> 


## -remarks



The <b>IOCSPPropertyCollection</b> contains attributes for the following:

<ul>
<li>Web proxy settings that include the  number of threads and number of cache entries</li>
<li>Audit settings that include start/stop, configuration change, security change, and request events</li>
<li>Security settings that include ACEs for <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> interfaces</li>
</ul>
All OCSP attribute information is stored in the following registry key:


<b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>OCSPSvc</b>\<b>Responder</b>



OCSP attributes govern OCSP responder service behavior for all CA configurations. For more information on CA configurations, see the <a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a> interface topic.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

