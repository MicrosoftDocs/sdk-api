---
UID: NS:ntdsapi.__unnamed_struct_10
title: DS_SITE_COST_INFO (ntdsapi.h)
author: windows-sdk-content
description: The DS_SITE_COST_INFO structure is used with the DsQuerySitesByCost function to contain communication cost data.
old-location: ad\ds_site_cost_info.htm
tech.root: ad
ms.assetid: 1920e824-992f-4d69-9b6d-586f58fa2ef7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDS_SITE_COST_INFO, DS_SITE_COST_INFO, DS_SITE_COST_INFO structure [Active Directory], ERROR_DS_OBJ_NOT_FOUND, ERROR_SUCCESS, ad.ds_site_cost_info, ntdsapi/DS_SITE_COST_INFO"
ms.topic: struct
f1_keywords: 
 - "ntdsapi/DS_SITE_COST_INFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_SITE_COST_INFO
targetos: Windows
req.typenames: DS_SITE_COST_INFO, *PDS_SITE_COST_INFO
req.redist: 
ms.custom: 19H1
---

# DS_SITE_COST_INFO structure


## -description


The <b>DS_SITE_COST_INFO</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a> function to contain communication cost data.


## -struct-fields




### -field errorCode

Contains a success or error code that indicates if the cost data for the site could  be obtained. This member can contain one of the following values.



#### ERROR_SUCCESS

The communication cost of the site was obtained and is contained in the <b>cost</b> member of this structure.



#### ERROR_DS_OBJ_NOT_FOUND

The communication cost of the site cannot be obtained. The <b>cost</b> member of this structure should be ignored.


### -field cost

If the <b>errorCode</b> member contains <b>ERROR_SUCCESS</b>, this member contains the communication cost value of the site. If the <b>errorCode</b> member contains <b>ERROR_DS_OBJ_NOT_FOUND</b>, this contents of this member is undefined.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">DC and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a>
 

 

