---
UID: NF:winldap.ldap_check_filterA
title: ldap_check_filterA function (winldap.h)
description: The ldap_check_filter function is used to verify filter syntax. (ANSI)
helpviewer_keywords: ["ldap.ldap__check__filter", "ldap_check_filterA", "winldap/ldap_check_filterA"]
old-location: ldap\ldap_check_filter.htm
tech.root: ldap
ms.assetid: 33b549bc-4b23-484a-a7cf-f4963154d492
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_check_filter, ldap.ldap__check__filter, ldap.ldap_check_filter, ldap_check_filter, ldap_check_filter function [LDAP], ldap_check_filterA, ldap_check_filterW, winldap/ldap_check_filter, winldap/ldap_check_filterA, winldap/ldap_check_filterW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_check_filterW (Unicode) and ldap_check_filterA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_check_filterA
 - winldap/ldap_check_filterA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_check_filter
 - ldap_check_filterA
 - ldap_check_filterW
---

# ldap_check_filterA function


## -description

The <b>ldap_check_filter</b> function is used to verify filter syntax.

## -parameters

### -param ld [in]

The session handle.

### -param SearchFilter [in]

A pointer to a wide, null-terminated string that contains the name of the filter to check.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Use <b>ldap_check_filter</b> to verify the syntax of a search filter before initiating a search. This syntax check does not perform a full verification of the search filter syntax against RFC 2254 rules. Rather, it verifies that the filter meets the minimum syntactic requirements for encoding required by the wldap32 search-filter-encoding routines. As a result, a search filter can pass an <b>ldap_check_filter</b> operation, and can be encoded by wldap32, but the server may still detect a RFC 2254 compliance violation and reject the search filter.





> [!NOTE]
> The winldap.h header defines ldap_check_filter as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search">ldap_search</a>
