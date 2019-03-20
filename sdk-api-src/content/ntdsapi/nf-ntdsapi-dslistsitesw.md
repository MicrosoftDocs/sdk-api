---
UID: NF:ntdsapi.DsListSitesW
title: DsListSitesW function (ntdsapi.h)
author: windows-sdk-content
description: Lists all the sites in the enterprise forest.
old-location: ad\dslistsites.htm
tech.root: ad
ms.assetid: d424e750-6700-42b8-9d4f-e430cd0a7e4e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsListSites, DsListSites function [Active Directory], DsListSitesA, DsListSitesW, _glines_dslistsites, ad.dslistsites, ntdsapi/DsListSites, ntdsapi/DsListSitesA, ntdsapi/DsListSitesW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsListSitesW function


## -description


The <b>DsListSites</b> function lists all the sites in the enterprise forest.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param ppSites [out]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure that receives the list of sites in the enterprise. The site name is returned in the distinguished name (DN) format. The returned structure must be freed using the 
<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a> function.


## -returns



If the function returns a list of sites, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>
 

 

