---
UID: NF:ntdsapi.DsFreeSpnArrayA
title: DsFreeSpnArrayA function (ntdsapi.h)
description: Frees an array returned from the DsGetSpn function. (ANSI)
helpviewer_keywords: ["DsFreeSpnArrayA", "ntdsapi/DsFreeSpnArrayA"]
old-location: ad\dsfreespnarray.htm
tech.root: ad
ms.assetid: 1c229933-432d-4ded-be3b-3bd339a0abe4
ms.date: 12/05/2018
ms.keywords: DsFreeSpnArray, DsFreeSpnArray function [Active Directory], DsFreeSpnArrayA, DsFreeSpnArrayW, _glines_dsfreespnarray, ad.dsfreespnarray, ntdsapi/DsFreeSpnArray, ntdsapi/DsFreeSpnArrayA, ntdsapi/DsFreeSpnArrayW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsFreeSpnArrayW (Unicode) and DsFreeSpnArrayA (ANSI)
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
 - DsFreeSpnArrayA
 - ntdsapi/DsFreeSpnArrayA
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
 - DsFreeSpnArray
 - DsFreeSpnArrayA
 - DsFreeSpnArrayW
---

# DsFreeSpnArrayA function


## -description

The <b>DsFreeSpnArray</b> function frees an array returned from the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a> function.

## -parameters

### -param cSpn [in]

Specifies the number of elements contained in <i>rpszSpn</i>.

### -param rpszSpn [in]

Pointer to an array returned from <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a>.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsFreeSpnArray as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
