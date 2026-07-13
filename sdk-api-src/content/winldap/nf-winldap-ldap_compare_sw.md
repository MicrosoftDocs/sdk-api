---
UID: NF:winldap.ldap_compare_sW
title: ldap_compare_sW function (winldap.h)
description: The ldap_compare_sW (Unicode) function (winldap.h) determines whether an attribute for a given entry holds a known value. 
helpviewer_keywords: ["_ldap_ldap_compare_s", "ldap.ldap__compare__s", "ldap.ldap_compare_s", "ldap_compare_s", "ldap_compare_s function [LDAP]", "ldap_compare_sW", "winldap/ldap_compare_s", "winldap/ldap_compare_sW"]
old-location: ldap\ldap_compare_s.htm
tech.root: ldap
ms.assetid: 44a7001d-d7ad-4b29-80bf-8d4b06e0fa43
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_compare_s, ldap.ldap__compare__s, ldap.ldap_compare_s, ldap_compare_s, ldap_compare_s function [LDAP], ldap_compare_sA, ldap_compare_sW, winldap/ldap_compare_s, winldap/ldap_compare_sA, winldap/ldap_compare_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_compare_sW (Unicode) and ldap_compare_sA (ANSI)
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
 - ldap_compare_sW
 - winldap/ldap_compare_sW
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
 - ldap_compare_s
 - ldap_compare_sA
 - ldap_compare_sW
---

# ldap_compare_sW function


## -description

Use the <b>ldap_compare_s</b> function to determine whether 
    an attribute for a given entry holds a known value.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry.

### -param attr [in]

A pointer to a null-terminated string that contains the attribute to compare.

### -param value [in]

A pointer to a null-terminated string that contains the string attribute value to compare to the attribute 
      value.

## -returns

If the function succeeds, and the attribute and known values match, the return value is 
       <b>LDAP_COMPARE_TRUE</b>. If the values do not match, the return value is 
       <b>LDAP_COMPARE_FALSE</b>.

If the function fails, it returns an error code. See 
       <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_compare_s</b> function initiates a synchronous 
    compare operation, comparing the value of an attribute to a known string value. Use 
    <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a> if you need to compare binary 
    values. Use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a> or 
    <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext">ldap_compare_ext</a> to carry out an asynchronous compare 
    operation.

Multithreading: Calls to <b>ldap_compare_s</b> are 
    thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
    <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
    <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines) before attempting any 
    other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_compare_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext">ldap_compare_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
