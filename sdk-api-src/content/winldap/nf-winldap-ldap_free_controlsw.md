---
UID: NF:winldap.ldap_free_controlsW
title: ldap_free_controlsW function (winldap.h)
description: The ldap_free_controlsW (Unicode) function (winldap.h) is an obsolete function which frees an array of LDAPControl structures.  
helpviewer_keywords: ["_ldap_ldap_free_controls", "ldap.ldap__free__controls", "ldap.ldap_free_controls", "ldap_free_controls", "ldap_free_controls function [LDAP]", "ldap_free_controlsW", "winldap/ldap_free_controls", "winldap/ldap_free_controlsW"]
old-location: ldap\ldap_free_controls.htm
tech.root: ldap
ms.assetid: 0c663189-5aa7-4dad-b265-c9af873bf576
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_free_controls, ldap.ldap__free__controls, ldap.ldap_free_controls, ldap_free_controls, ldap_free_controls function [LDAP], ldap_free_controlsA, ldap_free_controlsW, winldap/ldap_free_controls, winldap/ldap_free_controlsA, winldap/ldap_free_controlsW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_free_controlsW (Unicode) and ldap_free_controlsA (ANSI)
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
 - ldap_free_controlsW
 - winldap/ldap_free_controlsW
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
 - ldap_free_controls
 - ldap_free_controlsA
 - ldap_free_controlsW
---

# ldap_free_controlsW function


## -description

This function is not supported.

The <b>ldap_free_controls</b> function is an 
   obsolete function which frees an array of 
   <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures.
<div class="alert"><b>Note</b>  Obsolete. Use the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_controls_free">ldap_controls_free</a> 
    function.</div><div> </div>

## -parameters

### -param Controls [in]

The array of <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures to free.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
       <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

> [!NOTE]
> The winldap.h header defines ldap_free_controls as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
