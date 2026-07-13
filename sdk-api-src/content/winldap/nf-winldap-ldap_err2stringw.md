---
UID: NF:winldap.ldap_err2stringW
title: ldap_err2stringW function (winldap.h)
description: The ldap_err2stringW (Unicode) function (winldap.h) converts a numeric LDAP error code into a null-terminated character string that describes the error.
helpviewer_keywords: ["_ldap_ldap_err2string", "ldap.ldap__err2string", "ldap.ldap_err2string", "ldap_err2string", "ldap_err2string function [LDAP]", "ldap_err2stringW", "winldap/ldap_err2string", "winldap/ldap_err2stringW"]
old-location: ldap\ldap_err2string.htm
tech.root: ldap
ms.assetid: ebdccc79-e9c7-4a25-a1ab-01ba2b6f2d59
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_err2string, ldap.ldap__err2string, ldap.ldap_err2string, ldap_err2string, ldap_err2string function [LDAP], ldap_err2stringA, ldap_err2stringW, winldap/ldap_err2string, winldap/ldap_err2stringA, winldap/ldap_err2stringW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_err2stringW (Unicode) and ldap_err2stringA (ANSI)
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
 - ldap_err2stringW
 - winldap/ldap_err2stringW
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
 - ldap_err2string
 - ldap_err2stringA
 - ldap_err2stringW
---

# ldap_err2stringW function


## -description

The <b>ldap_err2string</b> function converts a numeric LDAP error code into a null-terminated character string that describes the error.

## -parameters

### -param err [in]

An LDAP error code as returned by another LDAP function.

## -returns

If the function succeeds, a pointer to a null-terminated character string that describes the error, is returned.

If the function fails, a pointer to <b>NULL</b> is returned.

## -remarks

Call <b>ldap_err2string</b> to convert any  numeric LDAP error code into an informative, null-terminated character string message that describes the error. Be aware that some of the asynchronous calls return -1. In this case, use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> to retrieve the LDAP error code, and then use <b>ldap_err2string</b> on that value.

The return value is a static pointer to the character string. Do not free this string.





> [!NOTE]
> The winldap.h header defines ldap_err2string as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>
