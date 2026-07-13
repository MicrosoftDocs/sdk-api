---
UID: NF:ntdsapi.DsRemoveDsDomainA
title: DsRemoveDsDomainA function (ntdsapi.h)
description: Removes all traces of a domain naming context from the global area of the directory service. (ANSI)
helpviewer_keywords: ["DsRemoveDsDomainA", "ntdsapi/DsRemoveDsDomainA"]
old-location: ad\dsremovedsdomain.htm
tech.root: ad
ms.assetid: 0639cc04-2821-4421-8aa7-363621c1d6b5
ms.date: 12/05/2018
ms.keywords: DsRemoveDsDomain, DsRemoveDsDomain function [Active Directory], DsRemoveDsDomainA, DsRemoveDsDomainW, _glines_dsremovedsdomain, ad.dsremovedsdomain, ntdsapi/DsRemoveDsDomain, ntdsapi/DsRemoveDsDomainA, ntdsapi/DsRemoveDsDomainW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsRemoveDsDomainA
 - ntdsapi/DsRemoveDsDomainA
dev_langs:
 - c++
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
---

# DsRemoveDsDomainA function


## -description

The <b>DsRemoveDsDomain</b> function removes all traces of a domain naming context from the global area of the directory service.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param DomainDN [in]

Pointer to a null-terminated string that specifies the distinguished name of the naming context to remove from the directory service.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful  or a Win32 or RPC error code if unsuccessful. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsremovedsservera">DsRemoveDsServer</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsRemoveDsDomain as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
