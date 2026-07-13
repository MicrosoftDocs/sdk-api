---
UID: NF:ntdsapi.DsQuerySitesByCostW
title: DsQuerySitesByCostW function (ntdsapi.h)
description: Gets the communication cost between one site and one or more other sites. (Unicode)
helpviewer_keywords: ["DsQuerySitesByCost", "DsQuerySitesByCost function [Active Directory]", "DsQuerySitesByCostW", "ad.dsquerysitesbycost", "ntdsapi/DsQuerySitesByCost", "ntdsapi/DsQuerySitesByCostW"]
old-location: ad\dsquerysitesbycost.htm
tech.root: ad
ms.assetid: 7a4cbd1c-8445-4882-8559-d44b6e5693e7
ms.date: 12/05/2018
ms.keywords: DsQuerySitesByCost, DsQuerySitesByCost function [Active Directory], DsQuerySitesByCostA, DsQuerySitesByCostW, ad.dsquerysitesbycost, ntdsapi/DsQuerySitesByCost, ntdsapi/DsQuerySitesByCostA, ntdsapi/DsQuerySitesByCostW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsQuerySitesByCostW (Unicode) and DsQuerySitesByCostA (ANSI)
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
 - DsQuerySitesByCostW
 - ntdsapi/DsQuerySitesByCostW
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
 - DsQuerySitesByCost
 - DsQuerySitesByCostA
 - DsQuerySitesByCostW
---

# DsQuerySitesByCostW function


## -description

The <b>DsQuerySitesByCost</b> function gets  the communication cost between one site and one or more other sites.

## -parameters

### -param hDS [in]

A directory service handle.

### -param pwszFromSite [in]

Pointer to a null-terminated string that contains the relative distinguished name of the site the costs are measured from.

### -param rgwszToSites [in]

Contains an array of null-terminated string pointers that contain the relative distinguished names of the sites the costs are measured to.

### -param cToSites [in]

Contains the number of elements in the <i>rgwszToSites</i> array.

### -param dwFlags [in]

Reserved.

### -param prgSiteInfo [out]

Pointer to an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_site_cost_info">DS_SITE_COST_INFO</a> structures that receives the cost data. Each element in this array contains the cost data between the site identified by the <i>pwszFromSite</i> parameter and the site identified by the corresponding <i>rgwszToSites</i> element.

The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesfree">DsQuerySitesFree</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise.
       Possible error codes include values listed in the following list.

## -remarks

The cost values obtained by this function are only used to compare and have no meaning by themselves. For example, the cost for site 1 can be compared to the cost for site 2, but the cost for site 1 cannot be compared to a fixed value.





> [!NOTE]
> The ntdsapi.h header defines DsQuerySitesByCost as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_site_cost_info">DS_SITE_COST_INFO</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesfree">DsQuerySitesFree</a>
