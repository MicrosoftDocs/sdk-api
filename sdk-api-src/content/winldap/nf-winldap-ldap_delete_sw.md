---
UID: NF:winldap.ldap_delete_sW
title: ldap_delete_sW function (winldap.h)
description: The ldap_delete_sW (Unicode) function (winldap.h) is a synchronous operation that removes a leaf entry from the directory tree.
helpviewer_keywords: ["_ldap_ldap_delete_s", "ldap.ldap__delete__s", "ldap.ldap_delete_s", "ldap_delete_s", "ldap_delete_s function [LDAP]", "ldap_delete_sW", "winldap/ldap_delete_s", "winldap/ldap_delete_sW"]
old-location: ldap\ldap_delete_s.htm
tech.root: ldap
ms.assetid: cded1b76-0fad-454f-bf5a-c500c9079f08
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_delete_s, ldap.ldap__delete__s, ldap.ldap_delete_s, ldap_delete_s, ldap_delete_s function [LDAP], ldap_delete_sA, ldap_delete_sW, winldap/ldap_delete_s, winldap/ldap_delete_sA, winldap/ldap_delete_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_delete_sW (Unicode) and ldap_delete_sA (ANSI)
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
 - ldap_delete_sW
 - winldap/ldap_delete_sW
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
 - ldap_delete_s
 - ldap_delete_sA
 - ldap_delete_sW
---

# ldap_delete_sW function


## -description

The <b>ldap_delete_s</b> function is a synchronous operation that removes a leaf entry from the directory tree.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_delete_s</b> to remove a leaf entry from the directory tree. Be aware that LDAP does not support deletion of entire subtrees in a single operation. As a synchronous operation, <b>ldap_delete_s</b> does not return until the operation is compete. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a> to perform the delete operation asynchronously.

Multithreading: The <b>ldap_delete_s</b> function is thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting any other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_delete_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
