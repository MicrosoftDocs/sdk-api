---
UID: NF:ntdsapi.DsListDomainsInSiteA
title: DsListDomainsInSiteA function (ntdsapi.h)
author: windows-sdk-content
description: Lists all the domains in a site.
old-location: ad\dslistdomainsinsite.htm
tech.root: ad
ms.assetid: 3a039c0c-ac5b-4455-960d-b26a207693ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsListDomainsInSite, DsListDomainsInSite function [Active Directory], DsListDomainsInSiteA, DsListDomainsInSiteW, _glines_dslistdomainsinsite, ad.dslistdomainsinsite, ntdsapi/DsListDomainsInSite, ntdsapi/DsListDomainsInSiteA, ntdsapi/DsListDomainsInSiteW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsListDomainsInSiteA function


## -description


The <b>DsListDomainsInSite</b> function lists all the domains in a site.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.


### -param site [in]

Pointer to a null-terminated string that specifies the site name. This string is taken from the list of site names returned by the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistsitesa">DsListSites</a> function.


### -param ppDomains [out]

Pointer to a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that receives the list of domains in the site. To free the returned structure, call 
the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a> function.


## -returns



If the function returns a list of domains, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
 

 

