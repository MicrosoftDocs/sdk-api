---
UID: NF:ntdsapi.DsListSitesW
title: DsListSitesW function (ntdsapi.h)
description: Lists all the sites in the enterprise forest. (Unicode)
helpviewer_keywords: ["DsListSites", "DsListSites function [Active Directory]", "DsListSitesW", "_glines_dslistsites", "ad.dslistsites", "ntdsapi/DsListSites", "ntdsapi/DsListSitesW"]
old-location: ad\dslistsites.htm
tech.root: ad
ms.assetid: d424e750-6700-42b8-9d4f-e430cd0a7e4e
ms.date: 12/05/2018
ms.keywords: DsListSites, DsListSites function [Active Directory], DsListSitesA, DsListSitesW, _glines_dslistsites, ad.dslistsites, ntdsapi/DsListSites, ntdsapi/DsListSitesA, ntdsapi/DsListSitesW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListSitesW (Unicode) and DsListSitesA (ANSI)
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
 - DsListSitesW
 - ntdsapi/DsListSitesW
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
 - DsListSites
 - DsListSitesA
 - DsListSitesW
---

# DsListSitesW function


## -description

The <b>DsListSites</b> function lists all the sites in the enterprise forest.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param ppSites [out]

Pointer to a pointer to a <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that receives the list of sites in the enterprise. The site name is returned in the distinguished name (DN) format. The returned structure must be freed using the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a> function.

## -returns

If the function returns a list of sites, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.

## -remarks

Individual name conversion errors are reported in the returned <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.





> [!NOTE]
> The ntdsapi.h header defines DsListSites as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
