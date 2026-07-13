---
UID: NF:winldap.ldap_addW
title: ldap_addW function (winldap.h)
description: The ldap_addW (Unicode) function (winldap.h) initiates an asynchronous add operation to a directory tree.
helpviewer_keywords: ["_ldap_ldap_add", "ldap.ldap__add", "ldap.ldap_add", "ldap_add", "ldap_add function [LDAP]", "ldap_addW", "winldap/ldap_add", "winldap/ldap_addW"]
old-location: ldap\ldap_add.htm
tech.root: ldap
ms.assetid: d978f668-7726-44e4-a0b1-31390e8498c4
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_add, ldap.ldap__add, ldap.ldap_add, ldap_add, ldap_add function [LDAP], ldap_addA, ldap_addW, winldap/ldap_add, winldap/ldap_addA, winldap/ldap_addW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_addW (Unicode) and ldap_addA (ANSI)
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
 - ldap_addW
 - winldap/ldap_addW
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
 - ldap_add
 - ldap_addA
 - ldap_addW
---

# ldap_addW function


## -description

The <b>ldap_add</b> function initiates an asynchronous add operation to a directory tree. For an add operation to succeed, the parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root).

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.

### -param attrs [in]

An array of pointers to 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Each structure specifies a single attribute.

## -returns

If the function succeeds, the message ID of the add operation is returned.

If the function fails, it returns –1 and sets the session error parameters in the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> data structure. To retrieve the error data, use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>.

## -remarks

Before calling <b>ldap_add</b>, create an entry by specifying its attributes in 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Set the <b>mod_op</b> member of each structure to LDAP_MOD_ADD, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry.

As an asynchronous function, <b>ldap_add</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has been completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

To have the results returned directly, use the synchronous function 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_s">ldap_add_s</a>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext">ldap_add_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext_s">ldap_add_ext_s</a> to enable support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_add</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_add as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/synchronous-vs--asynchronous-calls">Synchronous and Asynchronous Calls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext">ldap_add_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext_s">ldap_add_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_s">ldap_add_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
