---
UID: NF:ntdsapi.DsListServersForDomainInSiteW
title: DsListServersForDomainInSiteW function (ntdsapi.h)
description: Lists all the servers in a domain in a site. (Unicode)
helpviewer_keywords: ["DsListServersForDomainInSite", "DsListServersForDomainInSite function [Active Directory]", "DsListServersForDomainInSiteW", "_glines_dslistserversfordomaininsite", "ad.dslistserversfordomaininsite", "ntdsapi/DsListServersForDomainInSite", "ntdsapi/DsListServersForDomainInSiteW"]
old-location: ad\dslistserversfordomaininsite.htm
tech.root: ad
ms.assetid: 1e346532-bbbe-4b3b-a1cb-6a72319cb3e2
ms.date: 12/05/2018
ms.keywords: DsListServersForDomainInSite, DsListServersForDomainInSite function [Active Directory], DsListServersForDomainInSiteA, DsListServersForDomainInSiteW, _glines_dslistserversfordomaininsite, ad.dslistserversfordomaininsite, ntdsapi/DsListServersForDomainInSite, ntdsapi/DsListServersForDomainInSiteA, ntdsapi/DsListServersForDomainInSiteW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsListServersForDomainInSiteW
 - ntdsapi/DsListServersForDomainInSiteW
dev_langs:
 - c++
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
---

# DsListServersForDomainInSiteW function


## -description

The <b>DsListServersForDomainInSite</b> function lists all the servers in a domain in a site.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param domain [in]

Pointer to a null-terminated string that specifies the domain name. This string must be the same as one of the strings returned by <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistdomainsinsitea">DsListDomainsInSite</a> function.

### -param site [in]

Pointer to a null-terminated string that specifies the site name. This string is taken from the list of site names returned by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistsitesa">DsListSites</a> function.

### -param ppServers [out]

Pointer to a pointer to a 
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that receives the list of servers in the domain. The returned structure must be freed using 
the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a> function.

## -returns

If the function returns a list of servers, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.

## -remarks

Individual name conversion errors are reported in the returned <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.





> [!NOTE]
> The ntdsapi.h header defines DsListServersForDomainInSite as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
