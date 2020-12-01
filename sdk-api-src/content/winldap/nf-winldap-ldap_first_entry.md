---
UID: NF:winldap.ldap_first_entry
title: ldap_first_entry function (winldap.h)
description: The ldap_first_entry function returns the first entry of a message.
helpviewer_keywords: ["_ldap_ldap_first_entry","ldap.ldap__first__entry","ldap.ldap_first_entry","ldap_first_entry","ldap_first_entry function [LDAP]","winldap/ldap_first_entry"]
old-location: ldap\ldap_first_entry.htm
tech.root: ldap
ms.assetid: 1692d091-7963-492d-9998-5680a2a81088
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_first_entry, ldap.ldap__first__entry, ldap.ldap_first_entry, ldap_first_entry, ldap_first_entry function [LDAP], winldap/ldap_first_entry
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
 - ldap_first_entry
 - winldap/ldap_first_entry
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
 - ldap_first_entry
---

# ldap_first_entry function


## -description

The <b>ldap_first_entry</b> function returns the first entry of a message.

## -parameters

### -param ld [in]

The session handle.

### -param res [in]

The search result, as obtained by a call to one of the synchronous search routines or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -returns

If the search returned valid results, this function returns a pointer to the first result entry. If no entry or reference exists in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.

## -remarks

Use <b>ldap_first_entry</b> in conjunction with 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a> to step through and retrieve the list of entries from a search result chain.

You do not have to explicitly free the returned entry as it is freed when the message itself is freed.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>