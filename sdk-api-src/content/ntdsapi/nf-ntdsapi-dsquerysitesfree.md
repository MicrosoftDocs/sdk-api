---
UID: NF:ntdsapi.DsQuerySitesFree
title: DsQuerySitesFree function (ntdsapi.h)
author: windows-sdk-content
description: Frees the memory allocated by the DsQuerySitesByCost function.
old-location: ad\dsquerysitesfree.htm
tech.root: ad
ms.assetid: 810caa4f-8275-4ad8-ad3e-72061fc073dd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsQuerySitesFree, DsQuerySitesFree function [Active Directory], ad.dsquerysitesfree, ntdsapi/DsQuerySitesFree
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsQuerySitesFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsQuerySitesFree function


## -description


The <b>DsQuerySitesFree</b> function frees the memory allocated by the <a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a> function.


## -parameters




### -param rgSiteInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a> structures allocated by a call to <a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/1920e824-992f-4d69-9b6d-586f58fa2ef7">DS_SITE_COST_INFO</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/7a4cbd1c-8445-4882-8559-d44b6e5693e7">DsQuerySitesByCost</a>
 

 

