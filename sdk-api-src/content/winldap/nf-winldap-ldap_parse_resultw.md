---
UID: NF:winldap.ldap_parse_resultW
title: ldap_parse_resultW function (winldap.h)
description: The ldap_parse_resultW (Unicode) function (winldap.h) parses responses from the server and returns the appropriate fields. 
helpviewer_keywords: ["_ldap_ldap_parse_result", "ldap.ldap__parse__result", "ldap.ldap_parse_result", "ldap_parse_result", "ldap_parse_result function [LDAP]", "ldap_parse_resultW", "winldap/ldap_parse_result", "winldap/ldap_parse_resultW"]
old-location: ldap\ldap_parse_result.htm
tech.root: ldap
ms.assetid: 6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_parse_result, ldap.ldap__parse__result, ldap.ldap_parse_result, ldap_parse_result, ldap_parse_result function [LDAP], ldap_parse_resultA, ldap_parse_resultW, winldap/ldap_parse_result, winldap/ldap_parse_resultA, winldap/ldap_parse_resultW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_resultW (Unicode) and ldap_parse_resultA (ANSI)
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
 - ldap_parse_resultW
 - winldap/ldap_parse_resultW
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
 - ldap_parse_result
 - ldap_parse_resultA
 - ldap_parse_resultW
---

# ldap_parse_resultW function


## -description

The <b>ldap_parse_result</b> function parses responses from the server and returns the appropriate fields.

## -parameters

### -param Connection [in]

The session handle.

### -param ResultMessage [in]

The result of an LDAP operation as returned by one of the synchronous operation calls or by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> for an asynchronous operation.

### -param ReturnCode [out, optional]

Indicates the outcome of the server operation that generated the original result message. Pass <b>NULL</b> to ignore this field.

### -param MatchedDNs [out, optional]

A pointer to a wide, null-terminated string. In the case of a return of <b>LDAP_NO_SUCH_OBJECT</b>, this result parameter is filled in with a distinguished name indicating how much of the name in the request was recognized. Pass <b>NULL</b> to ignore this field.

### -param ErrorMessage [out, optional]

A pointer to a wide, null-terminated string that contains the contents of the error message field from the <i>ResultMessage</i> parameter. Pass <b>NULL</b> to ignore this field.

### -param Referrals [out, optional]

A pointer to a wide, null-terminated string that contains the contents of the referrals field from the <i>ResultMessage</i> parameter, indicating zero or more alternate LDAP servers where the request should be retried. Pass <b>NULL</b> to ignore this field.

### -param ServerControls [out, optional]

This result parameter is filled in with an allocated array of controls copied from the <i>ResultMessage</i> parameter.

### -param Freeit [in]

Determines whether the <i>ResultMessage</i> parameter is freed. You can pass any nonzero value to the <i>Freeit</i> parameter to free the <i>ResultMessage</i> pointer when it is no longer needed, or you can call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a> to free the result later.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_parse_result</b> function traverses a chain of server responses looking for result messages to parse. Use this function if you want to access the referrals, matching distinguished names, or server controls returned. The function skips over messages of type <b>LDAP_RES_SEARCH_ENTRY</b> and <b>LDAP_RES_SEARCH_REFERENCE</b>.

When they are no longer needed, free the <i>ErrorMessage</i> and <i>MatchedDNs</i> strings by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>. Free the <i>Referrals</i> array by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>. Free the <i>ServerControls</i> by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_controls_free">ldap_controls_free</a>.





> [!NOTE]
> The winldap.h header defines ldap_parse_result as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_controls_free">ldap_controls_free</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>
