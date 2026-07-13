---
UID: NF:winldap.ldap_modrdn2W
title: ldap_modrdn2W function (winldap.h)
description: The ldap_modrdn2W (Unicode) function (winldap.h) changes the relative distinguished name of an LDAP entry. 
helpviewer_keywords: ["_ldap_ldap_modrdn2", "ldap.ldap__modrdn2", "ldap.ldap_modrdn2", "ldap_modrdn2", "ldap_modrdn2 function [LDAP]", "ldap_modrdn2W", "winldap/ldap_modrdn2", "winldap/ldap_modrdn2W"]
old-location: ldap\ldap_modrdn2.htm
tech.root: ldap
ms.assetid: 7bf7370f-a5e6-474e-8fe9-e6895ef48ab5
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modrdn2, ldap.ldap__modrdn2, ldap.ldap_modrdn2, ldap_modrdn2, ldap_modrdn2 function [LDAP], ldap_modrdn2A, ldap_modrdn2W, winldap/ldap_modrdn2, winldap/ldap_modrdn2A, winldap/ldap_modrdn2W
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdn2W (Unicode) and ldap_modrdn2A (ANSI)
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
 - ldap_modrdn2W
 - winldap/ldap_modrdn2W
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
 - ldap_modrdn2
 - ldap_modrdn2A
 - ldap_modrdn2W
---

# ldap_modrdn2W function


## -description

The <b>ldap_modrdn2</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete. For LDAP 3 or later, use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a> functions.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param DistinguishedName [in]

A null-terminated string that contains the distinguished name to change.

### -param NewDistinguishedName [in]

A null-terminated string that contains the new relative distinguished name to give the entry.

### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.

## -returns

If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.

## -remarks

Use the <b>ldap_modrdn2</b> function, or its synchronous equivalent, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>, to change the name of an LDAP entry.

As an asynchronous function, <b>ldap_modrdn2</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

Be aware  that the various <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn">ldap_modrdn</a> functions enable you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation, which enables more general name-change access. This functionality is available by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>. These functions are recommended, instead of the <b>ldap_modrdn2</b> function, to change an entry name.

Multithreading: Calls to <b>ldap_modrdn2</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_modrdn2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>
