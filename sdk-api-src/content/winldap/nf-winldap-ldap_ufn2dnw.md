---
UID: NF:winldap.ldap_ufn2dnW
title: ldap_ufn2dnW function (winldap.h)
description: The ldap_ufn2dnW (Unicode) function (winldap.h) converts a user friendly name to a distinguished name.
helpviewer_keywords: ["_ldap_ldap_ufn2dn", "ldap.ldap__ufn2dn", "ldap.ldap_ufn2dn", "ldap_ufn2dn", "ldap_ufn2dn function [LDAP]", "ldap_ufn2dnW", "winldap/ldap_ufn2dn", "winldap/ldap_ufn2dnW"]
old-location: ldap\ldap_ufn2dn.htm
tech.root: ldap
ms.assetid: aca3942b-4371-48d2-8975-8d184abd1a49
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_ufn2dn, ldap.ldap__ufn2dn, ldap.ldap_ufn2dn, ldap_ufn2dn, ldap_ufn2dn function [LDAP], ldap_ufn2dnA, ldap_ufn2dnW, winldap/ldap_ufn2dn, winldap/ldap_ufn2dnA, winldap/ldap_ufn2dnW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_ufn2dnW (Unicode) and ldap_ufn2dnA (ANSI)
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
 - ldap_ufn2dnW
 - winldap/ldap_ufn2dnW
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
 - ldap_ufn2dn
 - ldap_ufn2dnA
 - ldap_ufn2dnW
---

# ldap_ufn2dnW function


## -description

The <b>ldap_ufn2dn</b> function converts a user-friendly name to a distinguished name.

## -parameters

### -param ufn [in]

Pointer to a null-terminated string that contains the user-friendly name to convert.

### -param pDn [out]

Pointer to a variable that receives a pointer to a null-terminated string that contains the resulting distinguished name.

If the <i>pDn</i> parameter returns non-<b>NULL</b>, free it with a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_ufn2dn</b> function attempts to normalize a user-specified name to a distinguished name. For example, consider an LDAP directory format for a common name of <i>LastName</i><b>, </b><i>FirstName</i>. Given a directory name of "Jeff Smith," <b>ldap_ufn2dn</b> will attempt to normalize this to "Smith, Jeff." The function follows RFC 1781; add CN= if not present, add OU= if none present, and so on. If it runs into any errors while normalizing, the function returns a copy of what was passed. It then allocates the output string from the LDAP memory pool.





> [!NOTE]
> The winldap.h header defines ldap_ufn2dn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>
