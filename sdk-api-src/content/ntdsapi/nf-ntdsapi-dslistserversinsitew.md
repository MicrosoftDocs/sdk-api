---
UID: NF:ntdsapi.DsListServersInSiteW
title: DsListServersInSiteW function
author: windows-sdk-content
description: Lists all the servers in a site.
old-location: ad\dslistserversinsite.htm
tech.root: ad
ms.assetid: 46773631-d464-4d9e-83e7-aa502599df71
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsListServersInSite, DsListServersInSite function [Active Directory], DsListServersInSiteA, DsListServersInSiteW, _glines_dslistserversinsite, ad.dslistserversinsite, ntdsapi/DsListServersInSite, ntdsapi/DsListServersInSiteA, ntdsapi/DsListServersInSiteW
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
req.unicode-ansi: DsListServersInSiteW (Unicode) and DsListServersInSiteA (ANSI)
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
 - DsListServersInSite
 - DsListServersInSiteA
 - DsListServersInSiteW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsListServersInSiteW function


## -description


The <b>DsListServersInSite</b> function lists all the servers in a site.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param site [in]

Pointer to a null-terminated string that specifies the site name. The site name uses a distinguished name format. It is taken from the list of sites returned by the <a href="https://msdn.microsoft.com/d424e750-6700-42b8-9d4f-e430cd0a7e4e">DsListSites</a> function.


### -param ppServers [out]

Pointer to a pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/ms676246(v=VS.85).aspx">DS_NAME_RESULT</a> structure that receives the list of servers in the site. The returned structure must be freed using 
the <a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a> function.


## -returns



If the function returns a list of servers, the return value is <b>NO_ERROR</b>. If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://msdn.microsoft.com/en-us/library/ms676246(v=VS.85).aspx">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms676246(v=VS.85).aspx">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>
 

 

