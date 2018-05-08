---
UID: NE:ntdsapi.DS_SPN_NAME_TYPE
title: DS_SPN_NAME_TYPE
author: windows-driver-content
description: The DS_SPN_NAME_TYPE enumeration is used by the DsGetSPN function to identify the format for composing SPNs.
old-location: ad\ds_spn_name_type.htm
old-project: AD
ms.assetid: 7aab22a6-1fe1-4127-97d3-54287d770790
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: DS_SPN_DNS_HOST, DS_SPN_DN_HOST, DS_SPN_DOMAIN, DS_SPN_NAME_TYPE, DS_SPN_NAME_TYPE enumeration [Active Directory], DS_SPN_NB_DOMAIN, DS_SPN_NB_HOST, DS_SPN_SERVICE, _glines_ds_spn_name_type, ad.ds__spn__name__type, ad.ds_spn_name_type, ntdsapi/DS_SPN_DNS_HOST, ntdsapi/DS_SPN_DN_HOST, ntdsapi/DS_SPN_DOMAIN, ntdsapi/DS_SPN_NAME_TYPE, ntdsapi/DS_SPN_NB_DOMAIN, ntdsapi/DS_SPN_NB_HOST, ntdsapi/DS_SPN_SERVICE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntdsapi.h
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
req.type-library: 
req.typenames: DS_SPN_NAME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_SPN_NAME_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

