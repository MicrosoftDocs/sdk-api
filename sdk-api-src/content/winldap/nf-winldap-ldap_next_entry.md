---
UID: NF:winldap.ldap_next_entry
title: ldap_next_entry function (winldap.h)
description: The ldap_next_entry function retrieves an entry from a search result chain.
helpviewer_keywords: ["_ldap_ldap_next_entry","ldap.ldap__next__entry","ldap.ldap_next_entry","ldap_next_entry","ldap_next_entry function [LDAP]","winldap/ldap_next_entry"]
old-location: ldap\ldap_next_entry.htm
tech.root: ldap
ms.assetid: a0920107-6f99-4d28-a12f-c7f952933472
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_next_entry, ldap.ldap__next__entry, ldap.ldap_next_entry, ldap_next_entry, ldap_next_entry function [LDAP], winldap/ldap_next_entry
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
 - ldap_next_entry
 - winldap/ldap_next_entry
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
 - ldap_next_entry
---

# ldap_next_entry function


## -description

The <b>ldap_next_entry</b> function retrieves an entry from a search result chain.

## -parameters

### -param ld [in]

The session handle.

### -param entry [in]

The entry returned by a previous call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> or <b>ldap_next_entry</b>.

## -returns

If the search returned valid results, this function returns a pointer to the next result entry in the results set. If no further entries or references exist in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.

## -remarks

Use <b>ldap_next_entry</b> in conjunction with 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> to step through and retrieve the list of entries from a search result chain.

You are not required to explicitly free the returned entry because it is freed when the message itself is freed.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>