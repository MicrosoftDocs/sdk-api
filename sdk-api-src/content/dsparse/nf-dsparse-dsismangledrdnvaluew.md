---
UID: NF:dsparse.DsIsMangledRdnValueW
title: DsIsMangledRdnValueW function (dsparse.h)
description: Determines if a given relative distinguished name value is a mangled name of the given type. (Unicode)
helpviewer_keywords: ["DsIsMangledRdnValue", "DsIsMangledRdnValue function [Active Directory]", "DsIsMangledRdnValueW", "_glines_dsismangledrdnvalue", "ad.dsismangledrdnvalue", "dsparse/DsIsMangledRdnValue", "dsparse/DsIsMangledRdnValueW"]
old-location: ad\dsismangledrdnvalue.htm
tech.root: ad
ms.assetid: adf5e133-9e48-4e97-af0c-4f8ea9b8bf8f
ms.date: 12/05/2018
ms.keywords: DsIsMangledRdnValue, DsIsMangledRdnValue function [Active Directory], DsIsMangledRdnValueA, DsIsMangledRdnValueW, _glines_dsismangledrdnvalue, ad.dsismangledrdnvalue, dsparse/DsIsMangledRdnValue, dsparse/DsIsMangledRdnValueA, dsparse/DsIsMangledRdnValueW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsIsMangledRdnValueW (Unicode) and DsIsMangledRdnValueA (ANSI)
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
 - DsIsMangledRdnValueW
 - dsparse/DsIsMangledRdnValueW
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
 - DsIsMangledRdnValue
 - DsIsMangledRdnValueA
 - DsIsMangledRdnValueW
---

# DsIsMangledRdnValueW function


## -description

The <b>DsIsMangledRdnValue</b> function determines if a given relative distinguished name value is a mangled name of the given type.

## -parameters

### -param pszRdn [in]

Pointer to a null-terminated string that contains  the relative distinguished name  to determine if it is mangled. The <i>cRdn</i> parameter contains the number of characters in this string.

### -param cRdn [in]

Contains the number of characters in the <i>pszRdn</i> string.

### -param eDsMangleForDesired [in]

Contains one of the <a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a> values that specifies the type of name mangling to search for.

## -returns

Returns <b>TRUE</b> if the  relative distinguished name is mangled and the mangle type is the same as specified. Returns <b>FALSE</b> if the relative distinguished name is not mangled or the  mangle type is different than specified.

## -remarks

This function determines if the given relative distinguished name value is mangled and mangled in the given type.  The <i>pszRdn</i> parameter should only contain the value of the relative distinguished name and not the key.  The relative distinguished name value may be quoted or unquoted.





> [!NOTE]
> The dsparse.h header defines DsIsMangledRdnValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsparse/ne-dsparse-ds_mangle_for">DS_MANGLE_FOR</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangleddna">DsIsMangledDn</a>
