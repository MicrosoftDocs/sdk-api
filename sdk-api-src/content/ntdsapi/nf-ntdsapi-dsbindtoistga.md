---
UID: NF:ntdsapi.DsBindToISTGA
title: DsBindToISTGA function (ntdsapi.h)
description: Binds to the computer that holds the Inter-Site Topology Generator (ISTG) role in the domain of the local computer. (ANSI)
helpviewer_keywords: ["DsBindToISTGA", "ntdsapi/DsBindToISTGA"]
old-location: ad\dsbindtoistg.htm
tech.root: ad
ms.assetid: bd53124c-8578-495d-b540-d4b4c09297c3
ms.date: 12/05/2018
ms.keywords: DsBindToISTG, DsBindToISTG function [Active Directory], DsBindToISTGA, DsBindToISTGW, ad.dsbindtoistg, ntdsapi/DsBindToISTG, ntdsapi/DsBindToISTGA, ntdsapi/DsBindToISTGW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindToISTGW (Unicode) and DsBindToISTGA (ANSI)
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
 - DsBindToISTGA
 - ntdsapi/DsBindToISTGA
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
 - DsBindToISTG
 - DsBindToISTGA
 - DsBindToISTGW
---

# DsBindToISTGA function


## -description

The <b>DsBindToISTG</b> function binds to the computer that holds the Inter-Site Topology Generator (ISTG) role in the domain of the local computer.

## -parameters

### -param SiteName [in, optional]

Pointer to a null-terminated string that contains the site name used when binding. If this parameter is <b>NULL</b>, the site of the nearest domain controller is used.

### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the bind handle. To close this handle, call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise.
       The following are possible error codes.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsBindToISTG as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
