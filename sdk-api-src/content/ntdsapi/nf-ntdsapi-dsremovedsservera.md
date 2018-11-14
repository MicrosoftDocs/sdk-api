---
UID: NF:ntdsapi.DsRemoveDsServerA
title: DsRemoveDsServerA function
author: windows-sdk-content
description: The DsRemoveDsServer function removes all traces of a directory service agent (DSA) from the global area of the directory service.
old-location: ad\dsremovedsserver.htm
tech.root: ad
ms.assetid: a79a2b71-10c7-495b-861f-0c7a4d86f720
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DsRemoveDsServer, DsRemoveDsServer function [Active Directory], DsRemoveDsServerA, DsRemoveDsServerW, _glines_dsremovedsserver, ad.dsremovedsserver, ntdsapi/DsRemoveDsServer, ntdsapi/DsRemoveDsServerA, ntdsapi/DsRemoveDsServerW
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
req.unicode-ansi: DsRemoveDsServerW (Unicode) and DsRemoveDsServerA (ANSI)
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
 - DsRemoveDsServer
 - DsRemoveDsServerA
 - DsRemoveDsServerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DsRemoveDsServerA
: 
---

# DsRemoveDsServerA function


## -description


The <b>DsRemoveDsServer</b> function removes all traces of a directory service agent (DSA) from the global area of the directory service.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param ServerDN [in]

Pointer to a null-terminated string that specifies the fully qualified distinguished name of the domain controller to remove.


### -param DomainDN [in, optional]

Pointer to a null-terminated string that specifies a domain hosted by <i>ServerDN</i>. If this parameter is <b>NULL</b>, no verification is performed to ensure that <i>ServerDN</i> is the last domain controller in <i>DomainDN</i>.


### -param fLastDcInDomain [out, optional]

Pointer to a Boolean value that receives <b>TRUE</b> if <i>ServerDN</i> is the last DC in <i>DomainDN</i> or <b>FALSE</b> otherwise. This parameter receives <b>FALSE</b> if <i>DomainDN</i> is <b>NULL</b>.


### -param fCommit [in]

Contains a Boolean value that specifies if the domain controller should actually be removed. If this parameter is nonzero, <i>ServerDN</i> is removed. If this parameter is zero, the existence of <i>ServerDN</i> is checked and <i>fLastDcInDomain</i> is written, but the domain controller is not removed.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful  or a Win32 or RPC error code if unsuccessful. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/0639cc04-2821-4421-8aa7-363621c1d6b5">DsRemoveDsDomain</a>
 

 

