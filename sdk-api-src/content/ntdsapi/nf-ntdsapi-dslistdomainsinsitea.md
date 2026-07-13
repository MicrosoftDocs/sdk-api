---
UID: NF:ntdsapi.DsListDomainsInSiteA
title: DsListDomainsInSiteA function (ntdsapi.h)
description: Lists all the domains in a site. (ANSI)
helpviewer_keywords: ["DsListDomainsInSiteA", "ntdsapi/DsListDomainsInSiteA"]
old-location: ad\dslistdomainsinsite.htm
tech.root: ad
ms.assetid: 3a039c0c-ac5b-4455-960d-b26a207693ed
ms.date: 12/05/2018
ms.keywords: DsListDomainsInSite, DsListDomainsInSite function [Active Directory], DsListDomainsInSiteA, DsListDomainsInSiteW, _glines_dslistdomainsinsite, ad.dslistdomainsinsite, ntdsapi/DsListDomainsInSite, ntdsapi/DsListDomainsInSiteA, ntdsapi/DsListDomainsInSiteW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListDomainsInSiteW (Unicode) and DsListDomainsInSiteA (ANSI)
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
 - DsListDomainsInSiteA
 - ntdsapi/DsListDomainsInSiteA
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
 - DsListDomainsInSite
 - DsListDomainsInSiteA
 - DsListDomainsInSiteW
---

# DsListDomainsInSiteA function


## -description

The <b>DsListDomainsInSite</b> function lists all the domains in a site.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param site [in]

Pointer to a null-terminated string that specifies the site name. This string is taken from the list of site names returned by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistsitesa">DsListSites</a> function.

### -param ppDomains [out]

Pointer to a pointer to a 
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that receives the list of domains in the site. To free the returned structure, call 
the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a> function.

## -returns

If the function returns a list of domains, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.

## -remarks

Individual name conversion errors are reported in the returned <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.





> [!NOTE]
> The ntdsapi.h header defines DsListDomainsInSite as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
