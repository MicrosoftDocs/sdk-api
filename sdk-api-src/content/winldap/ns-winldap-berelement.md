---
UID: NS:winldap.berelement
title: BerElement (winldap.h)
description: C++ class object that performs basic encoding rules (BER) encoding.
helpviewer_keywords: ["BerElement","BerElement structure [LDAP]","_ldap_berelement","ldap.berelement","winldap/BerElement"]
old-location: ldap\berelement.htm
tech.root: ldap
ms.assetid: 491bdf54-0b45-4324-93fc-35fe15155a3d
ms.date: 12/05/2018
ms.keywords: BerElement, BerElement structure [LDAP], _ldap_berelement, ldap.berelement, winldap/BerElement
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
req.typenames: BerElement
req.redist: 
ms.custom: 19H1
f1_keywords:
 - berelement
 - winldap/berelement
 - BerElement
 - winldap/BerElement
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
 - BerElement
---

# BerElement structure


## -description

A <b>BerElement</b> structure is a C++ class object that performs basic encoding rules (BER) encoding.

## -struct-fields

### -field opaque

Pointer to an opaque buffer. Do not attempt to access it.

## -remarks

This is an opaque data structure that the 
 <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a> function allocates and returns to indicate the current position during a traversal of an attribute list. Pass the pointer to this structure to the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a> function.

<div class="alert"><b>Caution</b>  When allocated by one of the two previous functions, you do not free the memory associated with this structure or its pointer when the <b>BerElement</b> is no longer required.</div>
<div> </div>
A <b>BerElement</b> structure can also be allocated by calling the <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_alloc_t">ber_alloc_t</a> or the <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_init">ber_init</a> function. In such cases, free the   memory allocated to the <b>BerElement</b> structure by using the <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>