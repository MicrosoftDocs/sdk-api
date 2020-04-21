---
UID: NF:ntdsapi.DsUnBindW
title: DsUnBindW function (ntdsapi.h)
description: The DsUnBind function finds an RPC session with a domain controller and unbinds a handle to the directory service (DS).helpviewer_keywords: ["DsUnBind","DsUnBind function [Active Directory]","DsUnBindA","DsUnBindW","_glines_dsunbind","ad.dsunbind","ntdsapi/DsUnBind","ntdsapi/DsUnBindA","ntdsapi/DsUnBindW"]
old-location: ad\dsunbind.htm
tech.root: ad
ms.assetid: 7106d67f-d421-4a7c-b775-440e5944f25e
ms.date: 12/05/2018
ms.keywords: DsUnBind, DsUnBind function [Active Directory], DsUnBindA, DsUnBindW, _glines_dsunbind, ad.dsunbind, ntdsapi/DsUnBind, ntdsapi/DsUnBindA, ntdsapi/DsUnBindW
f1_keywords:
- ntdsapi/DsUnBind
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsUnBindW function


## -description


The <b>DsUnBind</b> function finds an RPC session with a domain controller and unbinds a handle to the directory service (DS).


## -parameters




### -param phDS [in]

Pointer to a bind handle to the directory service. This handle is provided by a call to <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>.


## -returns



<b>NO_ERROR</b>




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>
 

 

