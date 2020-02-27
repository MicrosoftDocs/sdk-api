---
UID: NF:dsparse.DsIsMangledDnA
title: DsIsMangledDnA function (dsparse.h)
description: The DsIsMangledDn function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.
old-location: ad\dsismangleddn.htm
tech.root: ad
ms.assetid: e4aaa83c-3bd6-48db-9d34-367b76ba629c
ms.date: 12/05/2018
ms.keywords: DsIsMangledDn, DsIsMangledDn function [Active Directory], DsIsMangledDnA, DsIsMangledDnW, _glines_dsismangleddn, ad.dsismangleddn, dsparse/DsIsMangledDn, dsparse/DsIsMangledDnA, dsparse/DsIsMangledDnW
f1_keywords:
- dsparse/DsIsMangledDn
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsIsMangledDnA function


## -description


The <b>DsIsMangledDn</b> function determines if the first relative distinguished name (RDN) in a distinguished name (DN) is a mangled name of a given type.


## -parameters




### -param pszDn [in]

Pointer to a null-terminated string that contains the  distinguished name to retrieve the relative distinguished name from. This can also be a quoted distinguished name  as returned by other directory service functions.


### -param eDsMangleFor [in]

Contains one of the <a href="https://docs.microsoft.com/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a> values that specifies the type of name mangling to look for.


## -returns



Returns <b>TRUE</b> if the first relative distinguished name in <i>pszDn</i> is mangled in the manner specified by <i>eDsMangleFor</i> or <b>FALSE</b>  otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsparse/nf-dsparse-dsismangledrdnvaluea">DsIsMangledRdnValue</a>
 

 

