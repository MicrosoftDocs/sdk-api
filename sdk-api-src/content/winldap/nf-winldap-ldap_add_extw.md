---
UID: NF:winldap.ldap_add_extW
title: ldap_add_extW function (winldap.h)
description: The ldap_add_ext function initiates an asynchronous add operation to a tree. The parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root) for an add operation to succeed.
helpviewer_keywords: ["_ldap_ldap_add_ext","ldap.ldap__add__ext","ldap.ldap_add_ext","ldap_add_ext","ldap_add_ext function [LDAP]","ldap_add_extA","ldap_add_extW","winldap/ldap_add_ext","winldap/ldap_add_extA","winldap/ldap_add_extW"]
old-location: ldap\ldap_add_ext.htm
tech.root: ldap
ms.assetid: 13ad97e7-6d3c-43a6-b806-ec775abe303c
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_add_ext, ldap.ldap__add__ext, ldap.ldap_add_ext, ldap_add_ext, ldap_add_ext function [LDAP], ldap_add_extA, ldap_add_extW, winldap/ldap_add_ext, winldap/ldap_add_extA, winldap/ldap_add_extW
f1_keywords:
- winldap/ldap_add_ext
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
req.unicode-ansi: ldap_add_extW (Unicode) and ldap_add_extA (ANSI)
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
- ldap_add_ext
- ldap_add_extA
- ldap_add_extW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_add_extW function


## -description


The <b>ldap_add_ext</b> function initiates an asynchronous add operation to a tree. The parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root) for an add operation to succeed.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.


### -param attrs [in]

An array of pointers to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Each structure specifies a single attribute. For more information, see the Remarks section.


### -param ServerControls [in]

List of LDAP server controls.


### -param ClientControls [in]

List of client controls.


### -param MessageNumber [out]

The message ID for the request.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Error Handling</a>.




## -remarks



The parameters and effects of <b>ldap_add_ext</b> includes those of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add</a>. The extended routine includes additional parameters to support client and server controls and thread safety.

Before calling <b>ldap_add_ext</b>, create an entry by specifying its attributes in 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a> structures. Set the <b>mod_op</b> field of each structure to <b>LDAP_MOD_ADD</b>, and set the <b>mod_type</b> and <b>mod_vals</b> fields as appropriate for your entry.

If the operation succeeds, <b>ldap_add_ext</b> passes the message ID to the caller as a parameter. Call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation.

To have the results returned directly, use the synchronous function 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext_s">ldap_add_ext_s</a>.

Multithreaded: Calls to <b>ldap_add_ext</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>
<i>ServerControls</i> and <i>ClientControls</i> are optional and should be set to <b>NULL</b> if not used.





> [!NOTE]
> The winldap.h header defines ldap_add_ext as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Error Handling</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



Functions



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add_ext_s">ldap_add_ext_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
 

 

