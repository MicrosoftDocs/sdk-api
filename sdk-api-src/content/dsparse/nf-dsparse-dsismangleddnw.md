---
UID: NF:dsparse.DsIsMangledDnW
title: DsIsMangledDnW function (dsparse.h)
description: The DsIsMangledDn function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type. (Unicode)
helpviewer_keywords: ["DsIsMangledDn", "DsIsMangledDn function [Active Directory]", "DsIsMangledDnW", "_glines_dsismangleddn", "ad.dsismangleddn", "dsparse/DsIsMangledDn", "dsparse/DsIsMangledDnW"]
old-location: ad\dsismangleddn.htm
tech.root: ad
ms.assetid: e4aaa83c-3bd6-48db-9d34-367b76ba629c
ms.date: 12/05/2018
ms.keywords: DsIsMangledDn, DsIsMangledDn function [Active Directory], DsIsMangledDnA, DsIsMangledDnW, _glines_dsismangleddn, ad.dsismangleddn, dsparse/DsIsMangledDn, dsparse/DsIsMangledDnA, dsparse/DsIsMangledDnW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsIsMangledDnW (Unicode) and DsIsMangledDnA (ANSI)
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
 - DsIsMangledDnW
 - dsparse/DsIsMangledDnW
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
 - DsIsMangledDn
 - DsIsMangledDnA
 - DsIsMangledDnW
---

# DsIsMangledDnW function


## -description

The <b>DsIsMangledDn</b> function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.

## -parameters

### -param pszDn [in]

Pointer to a null-terminated string that contains the  distinguished name to retrieve the relative distinguished name from. This can also be a quoted distinguished name  as returned by other directory service functions.

### -param eDsMangleFor [in]

Contains one of the <a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a> values that specifies the type of name mangling to look for.

## -returns

Returns <b>TRUE</b> if the first relative distinguished name in <i>pszDn</i> is mangled in the manner specified by <i>eDsMangleFor</i> or <b>FALSE</b>  otherwise.

## -see-also

<a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangledrdnvaluea">DsIsMangledRdnValue</a>

## -remarks

> [!NOTE]
> The dsparse.h header defines DsIsMangledDn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
