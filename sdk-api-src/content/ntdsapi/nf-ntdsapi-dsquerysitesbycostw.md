---
UID: NF:ntdsapi.DsQuerySitesByCostW
title: DsQuerySitesByCostW function
author: windows-driver-content
description: Gets the communication cost between one site and one or more other sites.
old-location: ad\dsquerysitesbycost.htm
old-project: AD
ms.assetid: 7a4cbd1c-8445-4882-8559-d44b6e5693e7
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DsQuerySitesByCost, DsQuerySitesByCost function [Active Directory], DsQuerySitesByCostA, DsQuerySitesByCostW, ad.dsquerysitesbycost, ntdsapi/DsQuerySitesByCost, ntdsapi/DsQuerySitesByCostA, ntdsapi/DsQuerySitesByCostW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsQuerySitesByCost
-	DsQuerySitesByCostA
-	DsQuerySitesByCostW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DsQuerySitesByCostW function


## -description


The <b>DsQuerySitesByCost</b> function gets  the communication cost between one site and one or more other sites.


## -parameters




### -param hDS [in]

A directory service handle.


#### - pwszFromSite [in]

Pointer to a null-terminated string that contains the relative distinguished name of the site the costs are measured from.


#### - rgwszToSites [in]

Contains an array of null-terminated string pointers that contain the relative distinguished names of the sites the costs are measured to.


### -param cToSites [in]

Contains the number of elements in the <i>rgwszToSites</i> array.


### -param dwFlags [in]

Reserved.


### -param prgSiteInfo [out]

Pointer to an array of <a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a> structures that receives the cost data. Each element in this array contains the cost data between the site identified by the <i>pwszFromSite</i> parameter and the site identified by the corresponding <i>rgwszToSites</i> element.

The caller must free this memory when it is no longer required by calling <a href="https://msdn.microsoft.com/810caa4f-8275-4ad8-ad3e-72061fc073dd">DsQuerySitesFree</a>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise.
       Possible error codes include values listed in the following list.




## -remarks



The cost values obtained by this function are only used to compare and have no meaning by themselves. For example, the cost for site 1 can be compared to the cost for site 2, but the cost for site 1 cannot be compared to a fixed value.




## -see-also




<a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/810caa4f-8275-4ad8-ad3e-72061fc073dd">DsQuerySitesFree</a>
 

 

