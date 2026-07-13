---
UID: NF:winldap.ldap_add_sW
title: ldap_add_sW function (winldap.h)
description: The ldap_add_sW (Unicode) function (winldap.h) initiates a synchronous add operation that adds an entry to a tree.
helpviewer_keywords: ["_ldap_ldap_add_s", "ldap.ldap__add__s", "ldap.ldap_add_s", "ldap_add_s", "ldap_add_s function [LDAP]", "ldap_add_sW", "winldap/ldap_add_s", "winldap/ldap_add_sW"]
old-location: ldap\ldap_add_s.htm
tech.root: ldap
ms.assetid: 83ad8c35-92c4-4d73-93f5-f470655e8db5
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_add_s, ldap.ldap__add__s, ldap.ldap_add_s, ldap_add_s, ldap_add_s function [LDAP], ldap_add_sA, ldap_add_sW, winldap/ldap_add_s, winldap/ldap_add_sA, winldap/ldap_add_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_add_sW (Unicode) and ldap_add_sA (ANSI)
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
 - ldap_add_sW
 - winldap/ldap_add_sW
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
 - ldap_add_s
 - ldap_add_sA
 - ldap_add_sW
---

# ldap_add_sW function


## -description

The <b>ldap_add_s</b> function initiates a synchronous add operation that adds an entry to a tree. The parent of the entry being added must already exist or the parent must be empty (equal to the root distinguished name) for an add operation to succeed.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.

### -param attrs [in]

A null-terminated array of pointers to 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Each structure specifies a single attribute. See Remarks for more information.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

Before calling <b>ldap_add_s</b>. you must create an entry by specifying its attributes in 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Set the <b>mod_op</b> member of each structure to LDAP_MOD_ADD, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry. See 
<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a> for more information.

Upon completion of the add operation, <b>ldap_add_s</b> returns to the caller. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add</a> if you prefer to have the operation carried out asynchronously.

Multithreading: Calls to <b>ldap_add_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_add_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
