---
UID: NF:winldap.ldap_modrdnW
title: ldap_modrdnW function (winldap.h)
description: The ldap_modrdnW (Unicode) function (winldap.h) changes the relative distinguished name of an LDAP entry.
helpviewer_keywords: ["_ldap_ldap_modrdn", "ldap.ldap__modrdn", "ldap.ldap_modrdn", "ldap_modrdn", "ldap_modrdn function [LDAP]", "ldap_modrdnW", "winldap/ldap_modrdn", "winldap/ldap_modrdnW"]
old-location: ldap\ldap_modrdn.htm
tech.root: ldap
ms.assetid: 7a85eb4d-dcb1-4a5b-a7df-1d726215bde3
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modrdn, ldap.ldap__modrdn, ldap.ldap_modrdn, ldap_modrdn, ldap_modrdn function [LDAP], ldap_modrdnA, ldap_modrdnW, winldap/ldap_modrdn, winldap/ldap_modrdnA, winldap/ldap_modrdnW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdnW (Unicode) and ldap_modrdnA (ANSI)
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
 - ldap_modrdnW
 - winldap/ldap_modrdnW
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
 - ldap_modrdn
 - ldap_modrdnA
 - ldap_modrdnW
---

# ldap_modrdnW function


## -description

The <b>ldap_modrdn</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete and is provided for backward compatibility with earlier versions of LDAP. For LDAP 3 or later, use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a> functions.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to be changed.

### -param NewDistinguishedName [out]

A pointer to a null-terminated string that contains the new relative distinguished name to give the entry.

## -returns

If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.

## -remarks

Use the <b>ldap_modrdn</b> function, or its synchronous equivalent, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn_s">ldap_modrdn_s</a>, to change the name of an LDAP entry. LDAP 2 supports additional features through 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2">ldap_modrdn2</a> and 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>.

As an asynchronous function, <b>ldap_modrdn</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

Be aware that the various <b>ldap_modrdn</b> functions allow you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation that allows more general name change access. This feature is available by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>. These functions are  recommended, instead of the <b>ldap_modrdn</b> function, to change an entry name.

Multithreading: Calls to <b>ldap_modrdn</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations. <b>ldap_modrdn</b> is obsolete and provided solely for compatibility with LDAP 1 implementations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_modrdn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2">ldap_modrdn2</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn_s">ldap_modrdn_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
