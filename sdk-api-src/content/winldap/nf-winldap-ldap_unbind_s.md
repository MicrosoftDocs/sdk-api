---
UID: NF:winldap.ldap_unbind_s
title: ldap_unbind_s function (winldap.h)
description: The ldap_unbind_s function synchronously frees resources associated with an LDAP session.
helpviewer_keywords: ["_ldap_ldap_unbind_s","ldap.ldap__unbind__s","ldap.ldap_unbind_s","ldap_unbind_s","ldap_unbind_s function [LDAP]","winldap/ldap_unbind_s"]
old-location: ldap\ldap_unbind_s.htm
tech.root: ldap
ms.assetid: b4dcf3cc-d4cb-40ca-a57e-150d4008108c
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_unbind_s, ldap.ldap__unbind__s, ldap.ldap_unbind_s, ldap_unbind_s, ldap_unbind_s function [LDAP], winldap/ldap_unbind_s
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ldap_unbind_s
 - winldap/ldap_unbind_s
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
 - ldap_unbind_s
---

# ldap_unbind_s function


## -description

The <b>ldap_unbind_s</b> function synchronously frees resources associated with an LDAP session.

## -parameters

### -param ld [in]

The session handle.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_unbind_s</b> to unbind from the directory, close the connection, and dispose of the session handle.  Call this function when the  <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> connection structure is no longer required, even if you have not called 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> when opening the connection. Ensure that you do not inadvertently call this function more than once on a session handle because doing so can free resources that you did not intend to release.

Both 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> and <b>ldap_unbind_s</b> work synchronously. There is no server response to an unbind operation.

Multithreading: Calls to <b>ldap_unbind_s</b> are safe except that you cannot use the session handle to the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> structure after it has been freed.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>