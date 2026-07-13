---
UID: NF:winldap.ldap_rename_ext_sW
title: ldap_rename_ext_sW function (winldap.h)
description: The ldap_rename_ext_sW (Unicode) function (winldap.h) is a synchronous operation that changes the distinguished name of an entry in the directory.
helpviewer_keywords: ["_ldap_ldap_rename_ext_s", "ldap.ldap__rename__ext__s", "ldap.ldap_rename_ext_s", "ldap_rename_ext_s", "ldap_rename_ext_s function [LDAP]", "ldap_rename_ext_sW", "winldap/ldap_rename_ext_s", "winldap/ldap_rename_ext_sW"]
old-location: ldap\ldap_rename_ext_s.htm
tech.root: ldap
ms.assetid: 85a605f9-d075-4b1d-bfcb-a75c9e7f3023
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_rename_ext_s, ldap.ldap__rename__ext__s, ldap.ldap_rename_ext_s, ldap_rename_ext_s, ldap_rename_ext_s function [LDAP], ldap_rename_ext_sA, ldap_rename_ext_sW, winldap/ldap_rename_ext_s, winldap/ldap_rename_ext_sA, winldap/ldap_rename_ext_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_rename_ext_sW (Unicode) and ldap_rename_ext_sA (ANSI)
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
 - ldap_rename_ext_sW
 - winldap/ldap_rename_ext_sW
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
 - ldap_rename_ext_s
 - ldap_rename_ext_sA
 - ldap_rename_ext_sW
---

# ldap_rename_ext_sW function


## -description

The <b>ldap_rename_ext_s</b> function is a synchronous operation that changes the distinguished name of an entry in the directory. This function is available effective with LDAP 3.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the entry to be renamed.

### -param NewRDN [in]

A pointer to a wide, null-terminated string that contains the new relative distinguished name.

### -param NewParent [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the new parent for this entry. This parameter enables you to move the entry to a new parent container.

### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.

### -param ServerControls [in]

List of LDAP server controls.

### -param ClientControls [in]

List of client controls.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

Multithreading: Calls to <b>ldap_rename_ext_s</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_rename_ext_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>
