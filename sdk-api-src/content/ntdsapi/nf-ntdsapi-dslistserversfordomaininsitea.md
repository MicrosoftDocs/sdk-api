---
UID: NF:ntdsapi.DsListServersForDomainInSiteA
title: DsListServersForDomainInSiteA function (ntdsapi.h)
description: Lists all the servers in a domain in a site.
old-location: ad\dslistserversfordomaininsite.htm
tech.root: ad
ms.assetid: 1e346532-bbbe-4b3b-a1cb-6a72319cb3e2
ms.date: 12/05/2018
ms.keywords: DsListServersForDomainInSite, DsListServersForDomainInSite function [Active Directory], DsListServersForDomainInSiteA, DsListServersForDomainInSiteW, _glines_dslistserversfordomaininsite, ad.dslistserversfordomaininsite, ntdsapi/DsListServersForDomainInSite, ntdsapi/DsListServersForDomainInSiteA, ntdsapi/DsListServersForDomainInSiteW
ms.topic: function
f1_keywords:
- ntdsapi/DsListServersForDomainInSite
dev_langs:
- c++
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListServersForDomainInSiteW (Unicode) and DsListServersForDomainInSiteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntdsapi.dll
api_name:
- DsListServersForDomainInSite
- DsListServersForDomainInSiteA
- DsListServersForDomainInSiteW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsListServersForDomainInSiteA function


## -description


The <b>DsListServersForDomainInSite</b> function lists all the servers in a domain in a site.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.


### -param domain [in]

Pointer to a null-terminated string that specifies the domain name. This string must be the same as one of the strings returned by <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistdomainsinsitea">DsListDomainsInSite</a> function.


### -param site [in]

Pointer to a null-terminated string that specifies the site name. This string is taken from the list of site names returned by the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistsitesa">DsListSites</a> function.


### -param ppServers [out]

Pointer to a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that receives the list of servers in the domain. The returned structure must be freed using 
the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a> function.


## -returns



If the function returns a list of servers, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
 

 

