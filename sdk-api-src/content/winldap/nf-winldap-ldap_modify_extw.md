---
UID: NF:winldap.ldap_modify_extW
title: ldap_modify_extW function (winldap.h)
description: The ldap_modify_extW (Unicode) function (winldap.h) initiates an asynchronous operation to modify an existing entry. 
helpviewer_keywords: ["_ldap_ldap_modify_ext", "ldap.ldap__modify__ext", "ldap.ldap_modify_ext", "ldap_modify_ext", "ldap_modify_ext function [LDAP]", "ldap_modify_extW", "winldap/ldap_modify_ext", "winldap/ldap_modify_extW"]
old-location: ldap\ldap_modify_ext.htm
tech.root: ldap
ms.assetid: a11f4944-d574-4215-a25e-536adf21c469
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modify_ext, ldap.ldap__modify__ext, ldap.ldap_modify_ext, ldap_modify_ext, ldap_modify_ext function [LDAP], ldap_modify_extA, ldap_modify_extW, winldap/ldap_modify_ext, winldap/ldap_modify_extA, winldap/ldap_modify_extW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modify_extW (Unicode) and ldap_modify_extA (ANSI)
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
 - ldap_modify_extW
 - winldap/ldap_modify_extW
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
 - ldap_modify_ext
 - ldap_modify_extA
 - ldap_modify_extW
---

# ldap_modify_extW function


## -description

The <b>ldap_modify_ext</b> function changes an existing entry.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.

### -param mods [in]

A null-terminated array of modifications to make to the entry.

### -param ServerControls [in]

A list of LDAP server controls.

### -param ClientControls [in]

A list of client controls

### -param MessageNumber [out]

This result parameter is set to the message ID of the request if the call succeeds.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_modify_ext</b> function initiates an asynchronous operation to modify an existing entry. If values are being added or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, and no values remain, the function removes the attribute. All modifications are performed in the order in which they are listed.

The parameters and effects of <b>ldap_modify_ext</b> subsume those of 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify</a>. The extended routine includes additional parameters to support client and server controls, and thread safety.

If successful, <b>ldap_modify_ext</b> passes back the message ID for the operation in the <i>MessageNumber</i> parameter. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to obtain the result of the operation. If you prefer to have the function return the result directly, use the synchronous extended function 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s">ldap_modify_ext_s</a>.

Multithreading: Calls to <b>ldap_modify_ext</b> are thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_modify_ext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s">ldap_modify_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>
