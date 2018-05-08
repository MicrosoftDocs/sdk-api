---
UID: NF:ntdsapi.DsListDomainsInSiteA
title: DsListDomainsInSiteA function
author: windows-driver-content
description: Lists all the domains in a site.
old-location: ad\dslistdomainsinsite.htm
old-project: AD
ms.assetid: 3a039c0c-ac5b-4455-960d-b26a207693ed
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: DsListDomainsInSite, DsListDomainsInSite function [Active Directory], DsListDomainsInSiteA, DsListDomainsInSiteW, _glines_dslistdomainsinsite, ad.dslistdomainsinsite, ntdsapi/DsListDomainsInSite, ntdsapi/DsListDomainsInSiteA, ntdsapi/DsListDomainsInSiteW
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
req.unicode-ansi: DsListDomainsInSiteW (Unicode) and DsListDomainsInSiteA (ANSI)
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
-	DsListDomainsInSite
-	DsListDomainsInSiteA
-	DsListDomainsInSiteW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DsListDomainsInSiteA function


## -description


The <b>DsListDomainsInSite</b> function lists all the domains in a site.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param site [in]

Pointer to a null-terminated string that specifies the site name. This string is taken from the list of site names returned by the <a href="https://msdn.microsoft.com/d424e750-6700-42b8-9d4f-e430cd0a7e4e">DsListSites</a> function.


### -param ppDomains [out]

Pointer to a pointer to a 
<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure that receives the list of domains in the site. To free the returned structure, call 
the <a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a> function.


## -returns



If the function returns a list of domains, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>
 

 

