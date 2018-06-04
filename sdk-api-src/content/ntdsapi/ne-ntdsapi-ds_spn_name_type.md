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

# DS_SPN_NAME_TYPE enumeration


## -description


The <b>DS_SPN_NAME_TYPE</b> enumeration is used by the <a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSPN</a> function to identify the format for composing SPNs.


## -enum-fields




### -field DS_SPN_DNS_HOST

The SPN format for the distinguished name service of the host-based service, which provides services identified with its host computer. This SPN uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>jeffsmith.fabrikam.com</pre>
</td>
</tr>
</table></span></div>

### -field DS_SPN_DN_HOST

The SPN format for the distinguished name of the host-based service, which provides services identified with its host computer. This SPN uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>cn=jeffsmith,ou=computers,dc=fabrikam,dc=com</pre>
</td>
</tr>
</table></span></div>

### -field DS_SPN_NB_HOST

The SPN format for the NetBIOS service of the host-based service, which provides services identified with its host computer. This SPN uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>jeffsmith-nec</pre>
</td>
</tr>
</table></span></div>

### -field DS_SPN_DOMAIN

The SPN format for a replicable service that provides services to the specified domain. This SPN uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>fabrikam.com</pre>
</td>
</tr>
</table></span></div>

### -field DS_SPN_NB_DOMAIN

The SPN format for a replicable service that provides services to the specified NetBIOS domain. This SPN uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>fabrikam</pre>
</td>
</tr>
</table></span></div>

### -field DS_SPN_SERVICE

The SPN format for a specified service. This SPN uses the following formats, depending on which service is used:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>cn=anRpcService,cn=RPC Services,cn=system,dc=fabrikam,dc=com</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>cn=aWsService,cn=Winsock Services,cn=system,dc=fabrikam,dc=com</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>cn=aService,dc=itg,dc=fabrikam,dc=com</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>www.fabrikam.com, ftp.fabrikam.com, ldap.fabrikam.com</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>products.fabrikam.com</pre>
</td>
</tr>
</table></span></div>

## -see-also




<a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSPN</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

