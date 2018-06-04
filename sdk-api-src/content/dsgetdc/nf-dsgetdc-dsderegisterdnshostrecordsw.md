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

# DsDeregisterDnsHostRecordsW function


## -description


The <b>DsDeregisterDnsHostRecords</b> function deletes DNS entries, except for type A records registered by a domain controller. Only an administrator, account operator, or server operator may call this function.


## -parameters




### -param OPTIONAL

TBD


### -param DnsHostName [in]

Pointer to the null-terminated string that specifies the DNS host name of the domain controller whose DNS records are being deleted.


#### - DnsDomainName [in, optional]

The null-terminated string that specifies the DNS domain name of the domain occupied by the domain controller. It is unnecessary for this to be a domain hosted by this domain controller. If <b>NULL</b>, the <i>DnsHostName</i> with the leftmost label removed is specified.


#### - DomainGuid [in, optional]

Pointer to the Domain GUID of the domain. If <b>NULL</b>, GUID specific names are not removed.


#### - DsaGuid [in, optional]

Pointer to the GUID of the <b>NTDS-DSA</b> object to be deleted. If <b>NULL</b>, <b>NTDS-DSA</b> specific names are not removed.


#### - ServerName [in, optional]

The null-terminated string that specifies the name of the remote domain controller. Can be set to <b>NULL</b> if the calling application is running on the domain controller being updated.


## -returns



This function returns DSGETDCAPI DWORD.




## -remarks



This function deregisters SRV and CNAME records only. It leaves type A records intact. Deletion of site specific records, for example, _ldap._tcp._&lt;SiteName&gt;._sites.dc._msdcs.&lt;DnsDomainName&gt;, is attempted for every site (&lt;SiteName&gt; in this example) in the enterprise of the domain controller on which the function is executed. Therefore, this function call could create a time-consuming run and may generate significant network traffic for enterprises with many sites.




## -see-also




<a href="https://msdn.microsoft.com/e0f757d9-36b6-40f8-a1db-fb5b9862b46a">DsGetDcSiteCoverage</a>



<a href="https://msdn.microsoft.com/2dfffd9a-af4f-4a93-8b3c-966e4f7c455f">DsGetSiteName</a>
 

 

