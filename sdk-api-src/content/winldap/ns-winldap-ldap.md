---
UID: NS:winldap.ldap
title: LDAP (winldap.h)
description: Represents an LDAP session.
helpviewer_keywords: ["*PLDAP","LDAP","LDAP structure [LDAP]","PLDAP","PLDAP structure pointer [LDAP]","_ldap_ldap","ldap.ldap","winldap/LDAP","winldap/PLDAP"]
old-location: ldap\ldap.htm
tech.root: ldap
ms.assetid: 844093e1-daba-494d-91b3-67455ff2e456
ms.date: 12/05/2018
ms.keywords: '*PLDAP, LDAP, LDAP structure [LDAP], PLDAP, PLDAP structure pointer [LDAP], _ldap_ldap, ldap.ldap, winldap/LDAP, winldap/PLDAP'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAP, *PLDAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap
 - winldap/ldap
 - PLDAP
 - winldap/PLDAP
 - LDAP
 - winldap/LDAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAP
---

# LDAP structure


## -description

The <b>LDAP</b> structure represents an LDAP session. Typically, a session corresponds to a connection to a single server. However, in the case of referrals, an LDAP session may encompass several server connections. The ability to track referrals is available in LDAP 3.

## -struct-fields

## -remarks

An <b>LDAP</b> structure is an opaque data type allocated and initialized by a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-cldap_open">cldap_open</a>, or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>. Subsequent LDAP calls pass a handle to this structure, which maintains the state of an LDAP session for the duration of the connection. When the session ends, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> to destroy the connection handle.

Although this is an opaque data type, it is documented in Winldap.h. This is primarily of value in porting applications written using other LDAP client implementations. Call 
    <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> to access or change the values associated with the LDAP connection handle (this structure). Using these two functions also expose settings not directly accessible from the <b>LDAP</b> structure. For more information about session options, see <a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-cldap_open">cldap_open</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>