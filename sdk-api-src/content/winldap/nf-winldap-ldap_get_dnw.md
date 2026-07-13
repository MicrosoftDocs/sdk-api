---
UID: NF:winldap.ldap_get_dnW
title: ldap_get_dnW function (winldap.h)
description: The ldap_get_dnW (Unicode) function (winldap.h) retrieves the distinguished name for a given entry. 
helpviewer_keywords: ["_ldap_ldap_get_dn", "ldap.ldap__get__dn", "ldap.ldap_get_dn", "ldap_get_dn", "ldap_get_dn function [LDAP]", "ldap_get_dnW", "winldap/ldap_get_dn", "winldap/ldap_get_dnW"]
old-location: ldap\ldap_get_dn.htm
tech.root: ldap
ms.assetid: 00484fe7-65d2-4300-ab5c-0a69a25e65e6
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_get_dn, ldap.ldap__get__dn, ldap.ldap_get_dn, ldap_get_dn, ldap_get_dn function [LDAP], ldap_get_dnA, ldap_get_dnW, winldap/ldap_get_dn, winldap/ldap_get_dnA, winldap/ldap_get_dnW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_dnW (Unicode) and ldap_get_dnA (ANSI)
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
 - ldap_get_dnW
 - winldap/ldap_get_dnW
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
 - ldap_get_dn
 - ldap_get_dnA
 - ldap_get_dnW
---

# ldap_get_dnW function


## -description

The <b>ldap_get_dn</b> function retrieves the distinguished name for a given entry.

## -parameters

### -param ld [in]

The session handle.

### -param entry [in]

The entry whose distinguished name is to be retrieved.

## -returns

If the function succeeds, it returns the distinguished name as a pointer to a null-terminated character string.

If the function fails, it returns <b>NULL</b> and sets the session error parameters in the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> data structure.

## -remarks

The <b>ldap_get_dn</b> function retrieves the distinguished name for an entry that was returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>, or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>. When the returned name is no longer needed, free the string by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>.





> [!NOTE]
> The winldap.h header defines ldap_get_dn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>
