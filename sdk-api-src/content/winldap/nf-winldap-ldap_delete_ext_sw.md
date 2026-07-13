---
UID: NF:winldap.ldap_delete_ext_sW
title: ldap_delete_ext_sW function (winldap.h)
description: The ldap_delete_ext_sW (Unicode) function (winldap.h) is an extended routine that performs a synchronous operation to remove a leaf entry from the directory tree.
helpviewer_keywords: ["_ldap_ldap_delete_ext_s", "ldap.ldap__delete__ext__s", "ldap.ldap_delete_ext_s", "ldap_delete_ext_s", "ldap_delete_ext_s function [LDAP]", "ldap_delete_ext_sW", "winldap/ldap_delete_ext_s", "winldap/ldap_delete_ext_sW"]
old-location: ldap\ldap_delete_ext_s.htm
tech.root: ldap
ms.assetid: eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_delete_ext_s, ldap.ldap__delete__ext__s, ldap.ldap_delete_ext_s, ldap_delete_ext_s, ldap_delete_ext_s function [LDAP], ldap_delete_ext_sA, ldap_delete_ext_sW, winldap/ldap_delete_ext_s, winldap/ldap_delete_ext_sA, winldap/ldap_delete_ext_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_delete_ext_sW (Unicode) and ldap_delete_ext_sA (ANSI)
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
 - ldap_delete_ext_sW
 - winldap/ldap_delete_ext_sW
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
 - ldap_delete_ext_s
 - ldap_delete_ext_sA
 - ldap_delete_ext_sW
---

# ldap_delete_ext_sW function


## -description

The <b>ldap_delete_ext_s</b> function is an extended routine that performs a synchronous operation to remove a leaf entry from the directory tree.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.

### -param ServerControls [in]

Optional. List of LDAP server controls. Set this parameter to <b>NULL</b> if not used.

### -param ClientControls [in]

Optional. List of client controls. Set this parameter to <b>NULL</b> if not used.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_delete_ext_s</b> to remove a leaf entry from the directory tree. LDAP does not support deletion of entire subtrees in a single operation, however there is an extended control, <a href="/previous-versions/windows/desktop/ldap/ldap-server-tree-delete-oid">LDAP_SERVER_TREE_DELETE_OID</a>, that does provide this. The parameters and effects of <b>ldap_delete_ext_s</b> include those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_s">ldap_delete_s</a>. The extended routine includes additional parameters to support client and server controls and thread safety.

As a synchronous function, <b>ldap_delete_ext_s</b> returns when the delete operation is complete. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a> to have the delete operation performed asynchronously.

Multithreading: Calls to <b>ldap_delete_ext_s</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_delete_ext_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext">ldap_delete_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_s">ldap_delete_s</a>
