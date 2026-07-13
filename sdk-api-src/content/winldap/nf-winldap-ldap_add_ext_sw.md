---
UID: NF:winldap.ldap_add_ext_sW
title: ldap_add_ext_sW function (winldap.h)
description: The ldap_add_ext_sW (Unicode) function (winldap.h) initiates a synchronous add operation to a tree. 
helpviewer_keywords: ["_ldap_ldap_add_ext_s", "ldap.ldap__add__ext__s", "ldap.ldap_add_ext_s", "ldap_add_ext_s", "ldap_add_ext_s function [LDAP]", "ldap_add_ext_sW", "winldap/ldap_add_ext_s", "winldap/ldap_add_ext_sW"]
old-location: ldap\ldap_add_ext_s.htm
tech.root: ldap
ms.assetid: b124ad29-2f9a-48c4-b51e-2fc9143a630c
ms.date: 08/08/2022
ms.keywords: _ldap_ldap_add_ext_s, ldap.ldap__add__ext__s, ldap.ldap_add_ext_s, ldap_add_ext_s, ldap_add_ext_s function [LDAP], ldap_add_ext_sA, ldap_add_ext_sW, winldap/ldap_add_ext_s, winldap/ldap_add_ext_sA, winldap/ldap_add_ext_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_add_ext_sW (Unicode) and ldap_add_ext_sA (ANSI)
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
 - ldap_add_ext_sW
 - winldap/ldap_add_ext_sW
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
 - ldap_add_ext_s
 - ldap_add_ext_sA
 - ldap_add_ext_sW
---

# ldap_add_ext_sW function


## -description

The <b>ldap_add_ext_s</b> function initiates a synchronous add operation to a tree. For an add operation to succeed, the parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root).

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.

### -param attrs [in]

An array of pointers to 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Each structure specifies a single attribute. For more information, see the  Remarks section.

### -param ServerControls [in]

A list of LDAP server controls.

### -param ClientControls [in]

A list of client controls.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The parameters and effects of <b>ldap_add_ext_s</b> include those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_s">ldap_add_s</a>. The extended routine includes additional parameters to support client and server controls.

Before calling <b>ldap_add_ext_s</b>, create an entry by specifying its attributes in 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Set the <b>mod_op</b> member of the each structure to <b>LDAP_MOD_ADD</b>, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry.

Upon completion of the add operation, <b>ldap_add_ext_s</b> returns to the caller. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext">ldap_add_ext</a> if you prefer to have the operation completed asynchronously.

Multithreading: Calls to <b>ldap_add_ext_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>
<i>ServerControls</i> and <i>ClientControls</i> are optional and should be set to <b>NULL</b> if not used.





> [!NOTE]
> The winldap.h header defines ldap_add_ext_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext">ldap_add_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_s">ldap_add_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
