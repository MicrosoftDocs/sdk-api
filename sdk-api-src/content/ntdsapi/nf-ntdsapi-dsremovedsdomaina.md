---
UID: NF:ntdsapi.DsRemoveDsDomainA
title: DsRemoveDsDomainA function
author: windows-driver-content
description: Removes all traces of a domain naming context from the global area of the directory service.
old-location: ad\dsremovedsdomain.htm
old-project: AD
ms.assetid: 0639cc04-2821-4421-8aa7-363621c1d6b5
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: DsRemoveDsDomain, DsRemoveDsDomain function [Active Directory], DsRemoveDsDomainA, DsRemoveDsDomainW, _glines_dsremovedsdomain, ad.dsremovedsdomain, ntdsapi/DsRemoveDsDomain, ntdsapi/DsRemoveDsDomainA, ntdsapi/DsRemoveDsDomainW
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
req.unicode-ansi: DsRemoveDsDomainW (Unicode) and DsRemoveDsDomainA (ANSI)
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
-	DsRemoveDsDomain
-	DsRemoveDsDomainA
-	DsRemoveDsDomainW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DsRemoveDsDomainA function


## -description


The <b>DsRemoveDsDomain</b> function removes all traces of a domain naming context from the global area of the directory service.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param DomainDN [in]

Pointer to a null-terminated string that specifies the distinguished name of the naming context to remove from the directory service.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful  or a Win32 or RPC error code if unsuccessful. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/a79a2b71-10c7-495b-861f-0c7a4d86f720">DsRemoveDsServer</a>
 

 

