---
UID: NF:dsparse.DsCrackUnquotedMangledRdnA
title: DsCrackUnquotedMangledRdnA function (dsparse.h)
description: The DsCrackUnquotedMangledRdn function unmangles (unencodes) a given relative distinguished name and returns both the decoded GUID and the mangling type used. (ANSI)
helpviewer_keywords: ["DsCrackUnquotedMangledRdnA", "dsparse/DsCrackUnquotedMangledRdnA"]
old-location: ad\dscrackunquotedmangledrdn.htm
tech.root: ad
ms.assetid: 30711d2d-f541-46b4-a301-a0f9fc7d6676
ms.date: 12/05/2018
ms.keywords: DsCrackUnquotedMangledRdn, DsCrackUnquotedMangledRdn function [Active Directory], DsCrackUnquotedMangledRdnA, DsCrackUnquotedMangledRdnW, _glines_dscrackunquotedmangledrdn, ad.dscrackunquotedmangledrdn, dsparse/DsCrackUnquotedMangledRdn, dsparse/DsCrackUnquotedMangledRdnA, dsparse/DsCrackUnquotedMangledRdnW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsCrackUnquotedMangledRdnW (Unicode) and DsCrackUnquotedMangledRdnA (ANSI)
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
 - DsCrackUnquotedMangledRdnA
 - dsparse/DsCrackUnquotedMangledRdnA
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
 - DsCrackUnquotedMangledRdn
 - DsCrackUnquotedMangledRdnA
 - DsCrackUnquotedMangledRdnW
---

# DsCrackUnquotedMangledRdnA function


## -description

The <b>DsCrackUnquotedMangledRdn</b> function unmangles (unencodes) a given relative distinguished name and returns both the decoded GUID and the mangling type used.

## -parameters

### -param pszRDN [in]

Pointer to a string that contains the relative distinguished name (RDN) to translate. This string length is specified by the <i>cchRDN</i> parameter, so this string is not required to be null-terminated. This string must be in unquoted form. For more information about unquoted relative distinguished names, see 
<a href="/windows/desktop/api/dsparse/nf-dsparse-dsunquoterdnvaluea">DsUnquoteRdnValue</a>.

### -param cchRDN [in]

Contains the length, in characters, of the <i>pszRDN</i> string.

### -param pGuid [out, optional]

Pointer to <b>GUID</b> value that receives the GUID of the unmangled relative distinguished name.  This parameter can be <b>NULL</b>.

### -param peDsMangleFor [out, optional]

Pointer 
to a <a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a> value that receives the type of mangling used in the mangled relative distinguished name.  This parameter can be <b>NULL</b>.

## -returns

This function returns <b>TRUE</b> if the relative distinguished name is mangled or <b>FALSE</b> otherwise. If this function returns <b>FALSE</b>, neither <i>pGuid</i> or <i>peDsMangleFor</i> receive any data.

## -remarks

This function attempts to
    decode (unmangle)  an RDN that has been previously mangled due to a deletion or a naming conflict. If the relative distinguished name is mangled, the function returns <b>TRUE</b> and retrieves the GUID and mangle type, if requested.  If the relative distinguished name is not mangled, the function returns <b>FALSE</b>.





> [!NOTE]
> The dsparse.h header defines DsCrackUnquotedMangledRdn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangleddna">DsIsMangledDn</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangledrdnvaluea">DsIsMangledRdnValue</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsunquoterdnvaluea">DsUnquoteRdnValue</a>
