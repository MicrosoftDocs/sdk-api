---
UID: NF:ntdsapi.DsQuerySitesFree
title: DsQuerySitesFree function (ntdsapi.h)
description: Frees the memory allocated by the DsQuerySitesByCost function.
helpviewer_keywords: ["DsQuerySitesFree","DsQuerySitesFree function [Active Directory]","ad.dsquerysitesfree","ntdsapi/DsQuerySitesFree"]
old-location: ad\dsquerysitesfree.htm
tech.root: ad
ms.assetid: 810caa4f-8275-4ad8-ad3e-72061fc073dd
ms.date: 12/05/2018
ms.keywords: DsQuerySitesFree, DsQuerySitesFree function [Active Directory], ad.dsquerysitesfree, ntdsapi/DsQuerySitesFree
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
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsQuerySitesFree
 - ntdsapi/DsQuerySitesFree
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
 - DsQuerySitesFree
---

# DsQuerySitesFree function


## -description

The <b>DsQuerySitesFree</b> function frees the memory allocated by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a> function.

## -parameters

### -param rgSiteInfo [in]

Pointer to an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_site_cost_info">DS_SITE_COST_INFO</a> structures allocated by a call to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a>.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_site_cost_info">DS_SITE_COST_INFO</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a>