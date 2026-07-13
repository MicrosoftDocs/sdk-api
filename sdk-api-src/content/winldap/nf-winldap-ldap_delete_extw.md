---
UID: NF:winldap.ldap_delete_extW
title: ldap_delete_extW function (winldap.h)
description: The ldap_delete_extW (Unicode) function (winldap.h) is an extended routine that removes a leaf entry from the directory tree.
helpviewer_keywords: ["_ldap_ldap_delete_ext", "ldap.ldap__delete__ext", "ldap.ldap_delete_ext", "ldap_delete_ext", "ldap_delete_ext function [LDAP]", "ldap_delete_extW", "winldap/ldap_delete_ext", "winldap/ldap_delete_extW"]
old-location: ldap\ldap_delete_ext.htm
tech.root: ldap
ms.assetid: 65c4fa7c-76d8-47ec-b5c5-bf671529f5f1
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_delete_ext, ldap.ldap__delete__ext, ldap.ldap_delete_ext, ldap_delete_ext, ldap_delete_ext function [LDAP], ldap_delete_extA, ldap_delete_extW, winldap/ldap_delete_ext, winldap/ldap_delete_extA, winldap/ldap_delete_extW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_delete_extW (Unicode) and ldap_delete_extA (ANSI)
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
 - ldap_delete_extW
 - winldap/ldap_delete_extW
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
 - ldap_delete_ext
 - ldap_delete_extA
 - ldap_delete_extW
---

# ldap_delete_extW function


## -description

The <b>ldap_delete_ext</b> function is an extended routine that removes a leaf entry from the directory tree.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.

### -param ServerControls [in]

Optional. List of LDAP server controls. If not used, set this parameter to NULL.

### -param ClientControls [in]

Optional. List of client controls. If not used, set this parameter to <b>NULL</b>.

### -param MessageNumber [out]

Message ID for the request.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_delete_ext</b> function removes a leaf entry from the directory tree. LDAP does not support deletion of entire subtrees in a single operation, however there is an extended control, <a href="/previous-versions/windows/desktop/ldap/ldap-server-tree-delete-oid">LDAP_SERVER_TREE_DELETE_OID</a>, used to perform this operation.

The parameters and effects of <b>ldap_delete_ext</b> include those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a>. The extended routine includes parameters to support client and server controls and thread safety.

If the operation succeeds, <b>ldap_delete_ext</b> passes the message ID to the caller as a parameter when the operation returns successfully. To get the result of the operation, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID.

To have the function return the results directly, use the synchronous routine 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext_s">ldap_delete_ext_s</a>.

Multithreading: Calls to <b>ldap_delete_ext</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_delete_ext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete">ldap_delete</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_delete_ext_s">ldap_delete_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>
