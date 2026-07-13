---
UID: NF:winldap.ldap_modifyW
title: ldap_modifyW function (winldap.h)
description: The ldap_modifyW (Unicode) function (winldap.h) initiates an asynchronous operation to modify an existing entry.
helpviewer_keywords: ["_ldap_ldap_modify", "ldap.ldap__modify", "ldap.ldap_modify", "ldap_modify", "ldap_modify function [LDAP]", "ldap_modifyW", "winldap/ldap_modify", "winldap/ldap_modifyW"]
old-location: ldap\ldap_modify.htm
tech.root: ldap
ms.assetid: 93ae0af4-1b16-4bb0-952f-139241189d79
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modify, ldap.ldap__modify, ldap.ldap_modify, ldap_modify, ldap_modify function [LDAP], ldap_modifyA, ldap_modifyW, winldap/ldap_modify, winldap/ldap_modifyA, winldap/ldap_modifyW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modifyW (Unicode) and ldap_modifyA (ANSI)
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
 - ldap_modifyW
 - winldap/ldap_modifyW
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
 - ldap_modify
 - ldap_modifyA
 - ldap_modifyW
---

# ldap_modifyW function


## -description

The <b>ldap_modify</b> function changes an existing entry.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.

### -param mods [in]

A null-terminated array of modifications to make to the entry.

## -returns

If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> data structure.

## -remarks

The <b>ldap_modify</b> function initiates an asynchronous operation to modify an existing entry. If values are being added to or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, and no values remain, the function removes the attribute. All modifications are performed in the order in which they are listed.

As an asynchronous function, <b>ldap_modify</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

If you prefer to have the function return the results directly, use the synchronous routine 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s">ldap_modify_s</a>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext">ldap_modify_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s">ldap_modify_ext_s</a> if you need support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_modify</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_modify as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext">ldap_modify_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s">ldap_modify_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s">ldap_modify_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
