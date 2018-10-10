---
UID: NN:certadm.IOCSPPropertyCollection
title: IOCSPPropertyCollection
author: windows-sdk-content
description: Represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service.
old-location: security\iocsppropertycollection.htm
tech.root: seccrypto
ms.assetid: 8c700357-0cb4-4780-9ff1-ac57c46f9183
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IOCSPPropertyCollection, IOCSPPropertyCollection interface [Security], IOCSPPropertyCollection interface [Security],described, certadm/IOCSPPropertyCollection, security.iocsppropertycollection
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPPropertyCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPPropertyCollection interface


## -description


The <b>IOCSPPropertyCollection</b> interface represents a set of configurable attribute properties (name-value pairs) for an Online Certificate Status Protocol (OCSP) service. Microsoft provides a default implementation of this interface in the <b>OCSPPropertyCollection</b> class.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_OCSPPropertyCollection</b> class identifier.

In Visual Basic Scripting Edition, you create an instance of the <b>OCSPPropertyCollection</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOCSPPropertyCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IOCSPPropertyCollection</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa386403(v=VS.85).aspx">CreateProperty</a>
</td>
<td align="left" width="63%">
Creates a new property and adds it to a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa386407(v=VS.85).aspx">DeleteProperty</a>
</td>
<td align="left" width="63%">
Removes a named property from a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa386410(v=VS.85).aspx">GetAllProperties</a>
</td>
<td align="left" width="63%">
Gets all properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa386413(v=VS.85).aspx">InitializeFromProperties</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa386468(v=VS.85).aspx">_NewEnum</a>


</td>
<td align="left" width="63%">
Gets an enumerator for a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa386399(v=VS.85).aspx">Count</a>


</td>
<td align="left" width="63%">
Gets the number of properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa386423(v=VS.85).aspx">Item</a>


</td>
<td align="left" width="63%">
Gets the property identified by index  in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa386417(v=VS.85).aspx">ItemByName</a>


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
<li>Security settings that include ACEs for <a href="https://msdn.microsoft.com/en-us/library/Aa386313(v=VS.85).aspx">IOCSPAdmin</a> interfaces</li>
</ul>
All OCSP attribute information is stored in the following registry key:


<b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>OCSPSvc</b>\<b>Responder</b>



OCSP attributes govern OCSP responder service behavior for all CA configurations. For more information on CA configurations, see the <a href="https://msdn.microsoft.com/en-us/library/Aa386328(v=VS.85).aspx">IOCSPCAConfiguration</a> interface topic.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

