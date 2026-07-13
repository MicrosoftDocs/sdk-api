---
UID: NF:winldap.ldap_dn2ufnW
title: ldap_dn2ufnW function (winldap.h)
description: The ldap_dn2ufnW (Unicode) function (winldap.h) converts a distinguished name to a user-friendly format. 
helpviewer_keywords: ["_ldap_ldap_dn2ufn", "ldap.ldap__dn2ufn", "ldap.ldap_dn2ufn", "ldap_dn2ufn", "ldap_dn2ufn function [LDAP]", "ldap_dn2ufnW", "winldap/ldap_dn2ufn", "winldap/ldap_dn2ufnW"]
old-location: ldap\ldap_dn2ufn.htm
tech.root: ldap
ms.assetid: 6c9c943f-304a-496c-bac4-283b6c717774
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_dn2ufn, ldap.ldap__dn2ufn, ldap.ldap_dn2ufn, ldap_dn2ufn, ldap_dn2ufn function [LDAP], ldap_dn2ufnA, ldap_dn2ufnW, winldap/ldap_dn2ufn, winldap/ldap_dn2ufnA, winldap/ldap_dn2ufnW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_dn2ufnW (Unicode) and ldap_dn2ufnA (ANSI)
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
 - ldap_dn2ufnW
 - winldap/ldap_dn2ufnW
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
 - ldap_dn2ufn
 - ldap_dn2ufnA
 - ldap_dn2ufnW
---

# ldap_dn2ufnW function


## -description

The <b>ldap_dn2ufn</b> function converts a distinguished name to a user-friendly format.

## -parameters

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name to convert.

## -returns

If the function is successful, the user-friendly name is returned as a pointer to a null-terminated character string.

If the function fails, <b>NULL</b> is returned.

## -remarks

When given an entry distinguished name, <b>ldap_dn2ufn</b> returns a null-terminated character string that contains the entry name in a user-friendly format. The composition of the user-friendly format is based on the format described in RFC 1781, and depends upon the directory service implementation and the type of entry. The return value remains in memory-allocated space until you call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>.





> [!NOTE]
> The winldap.h header defines ldap_dn2ufn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>
