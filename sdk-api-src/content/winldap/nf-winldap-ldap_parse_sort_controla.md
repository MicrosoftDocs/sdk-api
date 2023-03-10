---
UID: NF:winldap.ldap_parse_sort_controlA
title: ldap_parse_sort_controlA function (winldap.h)
description: The ldap_parse_sort_control function parses the sort control returned by the server. (ldap_parse_sort_controlA)
helpviewer_keywords: ["ldap.ldap__parse__sort__control", "ldap_parse_sort_controlA", "winldap/ldap_parse_sort_controlA"]
old-location: ldap\ldap_parse_sort_control.htm
tech.root: ldap
ms.assetid: 71d6bae2-3ee4-417c-8c1b-d277cad03f36
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_parse_sort_control, ldap.ldap__parse__sort__control, ldap.ldap_parse_sort_control, ldap_parse_sort_control, ldap_parse_sort_control function [LDAP], ldap_parse_sort_controlA, ldap_parse_sort_controlW, winldap/ldap_parse_sort_control, winldap/ldap_parse_sort_controlA, winldap/ldap_parse_sort_controlW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_sort_controlW (Unicode) and ldap_parse_sort_controlA (ANSI)
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
 - ldap_parse_sort_controlA
 - winldap/ldap_parse_sort_controlA
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
 - ldap_parse_sort_control
 - ldap_parse_sort_controlA
 - ldap_parse_sort_controlW
---

# ldap_parse_sort_controlA function


## -description

The <b>ldap_parse_sort_control</b> function parses the sort control returned by the server.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param Control [in]

The control returned from the server, as obtained from a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>.

### -param Result [out]

The result code.

### -param Attribute [out]

A pointer to a null-terminated string that contains the name of the attribute that caused the operation to fail.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

When the server returns the results, it returns a control in the SearchResultDone message. Call <b>ldap_parse_sort_control</b> to parse this sort control.

If the sort operation failed, the server may return the name of the attribute that caused the failure. In this case, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a> to free the attribute value

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>
