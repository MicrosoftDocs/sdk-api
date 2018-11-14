---
UID: NF:ntdsapi.DsUnBindA
title: DsUnBindA function
author: windows-sdk-content
description: The DsUnBind function finds an RPC session with a domain controller and unbinds a handle to the directory service (DS).
old-location: ad\dsunbind.htm
tech.root: ad
ms.assetid: 7106d67f-d421-4a7c-b775-440e5944f25e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DsUnBind, DsUnBind function [Active Directory], DsUnBindA, DsUnBindW, _glines_dsunbind, ad.dsunbind, ntdsapi/DsUnBind, ntdsapi/DsUnBindA, ntdsapi/DsUnBindW
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
req.unicode-ansi: DsUnBindW (Unicode) and DsUnBindA (ANSI)
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
 - KernelBase.dll
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsUnBind
 - DsUnBindA
 - DsUnBindW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DsUnBindA
: 
---

# DsUnBindA function


## -description


The <b>DsUnBind</b> function finds an RPC session with a domain controller and unbinds a handle to the directory service (DS).


## -parameters




### -param phDS [in]

Pointer to a bind handle to the directory service. This handle is provided by a call to <a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>, <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>, or <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>.


## -returns



<b>NO_ERROR</b>




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>
 

 

