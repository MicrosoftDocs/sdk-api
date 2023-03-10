---
UID: NF:winber.ber_free
title: ber_free function (winber.h)
description: The ber_free function frees a BerElement structure that was previously allocated with ber_alloc_t, ber_init, or the ldap_first_attribute/ ldap_next_attribute search functions.
helpviewer_keywords: ["_ldap_ber_free","ber_free","ber_free function [LDAP]","ldap.ber__free","ldap.ber_free","winber/ber_free"]
old-location: ldap\ber_free.htm
tech.root: ldap
ms.assetid: b0f5a81e-a1d1-41c3-802c-b17be2275964
ms.date: 12/05/2018
ms.keywords: _ldap_ber_free, ber_free, ber_free function [LDAP], ldap.ber__free, ldap.ber_free, winber/ber_free
req.header: winber.h
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
 - ber_free
 - winber/ber_free
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
 - ber_free
---

# ber_free function


## -description

The <b>ber_free</b> function frees a 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure that was previously allocated with 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_alloc_t">ber_alloc_t</a>, 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_init">ber_init</a>, or the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>/
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a> search functions.

## -parameters

### -param pBerElement [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure to be deallocated.

### -param fbuf [in]

Must be set to 0 if freeing structures allocated by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>/
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>, otherwise it must be set to 1.

## -returns

None.

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_alloc_t">ber_alloc_t</a>