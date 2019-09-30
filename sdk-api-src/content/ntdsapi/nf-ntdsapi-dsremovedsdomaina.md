---
UID: NF:ntdsapi.DsRemoveDsDomainA
title: DsRemoveDsDomainA function (ntdsapi.h)
author: windows-sdk-content
description: Removes all traces of a domain naming context from the global area of the directory service.
old-location: ad\dsremovedsdomain.htm
tech.root: ad
ms.assetid: 0639cc04-2821-4421-8aa7-363621c1d6b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsRemoveDsDomain, DsRemoveDsDomain function [Active Directory], DsRemoveDsDomainA, DsRemoveDsDomainW, _glines_dsremovedsdomain, ad.dsremovedsdomain, ntdsapi/DsRemoveDsDomain, ntdsapi/DsRemoveDsDomainA, ntdsapi/DsRemoveDsDomainW
ms.topic: function
f1_keywords: 
 - "ntdsapi/DsRemoveDsDomain"
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsRemoveDsDomainW (Unicode) and DsRemoveDsDomainA (ANSI)
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
 - DsRemoveDsDomain
 - DsRemoveDsDomainA
 - DsRemoveDsDomainW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsRemoveDsDomainA function


## -description


The <b>DsRemoveDsDomain</b> function removes all traces of a domain naming context from the global area of the directory service.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.


### -param DomainDN [in]

Pointer to a null-terminated string that specifies the distinguished name of the naming context to remove from the directory service.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful  or a Win32 or RPC error code if unsuccessful. Possible error codes include the following.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsremovedsservera">DsRemoveDsServer</a>
 

 

