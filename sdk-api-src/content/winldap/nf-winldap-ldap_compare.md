---
UID: NF:winldap.ldap_compare
title: ldap_compare function (winldap.h)
description: Use the ldap_compare function to determine whether an attribute for a given entry holds a known value.helpviewer_keywords: ["_ldap_ldap_compare","ldap.ldap__compare","ldap.ldap_compare","ldap_compare","ldap_compare function [LDAP]","ldap_compareA","ldap_compareW","winldap/ldap_compare","winldap/ldap_compareA","winldap/ldap_compareW"]
old-location: ldap\ldap_compare.htm
tech.root: ldap
ms.assetid: 0cdcea2f-5ee2-407a-a229-5a3fb1e3b856
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_compare, ldap.ldap__compare, ldap.ldap_compare, ldap_compare, ldap_compare function [LDAP], ldap_compareA, ldap_compareW, winldap/ldap_compare, winldap/ldap_compareA, winldap/ldap_compareW
f1_keywords:
- winldap/ldap_compare
dev_langs:
- c++
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_compareW (Unicode) and ldap_compareA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wldap32.dll
api_name:
- ldap_compare
- ldap_compareA
- ldap_compareW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_compare function


## -description


Use the <b>ldap_compare</b> function to determine whether an attribute for a given entry holds a known value.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry.


### -param attr [in]

A pointer to a null-terminated string that contains the attribute to compare.


### -param value [in]

A pointer to a null-terminated string that contains the string attribute value to compare to the attribute value.


## -returns



If the function succeeds, the message ID of the compare operation is returned.

If the function fails, it returns –1 and sets the session error parameters in the LDAP structure. This error can then be retrieved using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>.




## -remarks



The <b>ldap_compare</b> function initiates an asynchronous compare operation, comparing the value of an attribute to a known string value. Use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext">ldap_compare_ext</a> or 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a> to compare binary values. Use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_s">ldap_compare_s</a> or <b>ldap_compare_ext_s</b> to perform a synchronous compare operation.

As an asynchronous function, <b>ldap_compare</b> returns a message ID for the operation. Call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation before it has been completed, call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

To have the function return the results directly, use the synchronous routine 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_s">ldap_compare_s</a>. Use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext">ldap_compare_ext</a> or 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a> to enable support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_compare</b> are thread-safe, provided that 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to get the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext">ldap_compare_ext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_s">ldap_compare_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
 

 

