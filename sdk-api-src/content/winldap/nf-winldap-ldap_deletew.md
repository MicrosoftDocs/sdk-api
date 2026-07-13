---
UID: NF:winldap.ldap_deleteW
title: ldap_deleteW function (winldap.h)
description: The ldap_deleteW (Unicode) function (winldap.h) deletes an entry from the directory tree. 
helpviewer_keywords: ["_ldap_ldap_delete", "ldap.ldap__delete", "ldap.ldap_delete", "ldap_delete", "ldap_delete function [LDAP]", "ldap_deleteW", "winldap/ldap_delete", "winldap/ldap_deleteW"]
old-location: ldap\ldap_delete.htm
tech.root: ldap
ms.assetid: 314f3128-ab09-45a7-a678-779d5b7d4d72
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_delete, ldap.ldap__delete, ldap.ldap_delete, ldap_delete, ldap_delete function [LDAP], ldap_deleteA, ldap_deleteW, winldap/ldap_delete, winldap/ldap_deleteA, winldap/ldap_deleteW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_deleteW (Unicode) and ldap_deleteA (ANSI)
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
 - ldap_deleteW
 - winldap/ldap_deleteW
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
 - ldap_delete
 - ldap_deleteA
 - ldap_deleteW
---

# ldap_deleteW function


## -description

The <b>ldap_delete</b> function deletes an entry from the directory tree.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.

## -returns

If the function succeeds, it returns the message ID of the delete operation.

If the function fails, the return value is –1 and the function sets the session error parameters in the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> data structure. To retrieve this value, use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>.

## -remarks

Call <b>ldap_delete</b> to remove a leaf entry from the directory tree. Be aware that LDAP does not support deletion of entire subtrees in a single operation. As an asynchronous function, <b>ldap_delete</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous delete operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

To have the function return the results directly, use the synchronous routine 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_s">ldap_delete_s</a>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext_s">ldap_delete_ext_s</a> to enable support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_delete</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting any other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_delete as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext_s">ldap_delete_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_s">ldap_delete_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
