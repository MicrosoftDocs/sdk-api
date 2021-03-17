---
UID: NF:winber.ber_skip_tag
title: ber_skip_tag function (winber.h)
description: The ber_skip_tag function skips the current tag and returns the tag of the next element in the supplied BerElement structure.
helpviewer_keywords: ["_ldap_ber_skip_tag","ber_skip_tag","ber_skip_tag function [LDAP]","ldap.ber__skip__tag","ldap.ber_skip_tag","winber/ber_skip_tag"]
old-location: ldap\ber_skip_tag.htm
tech.root: ldap
ms.assetid: aa7548db-7752-4ce5-9f24-434abe77b000
ms.date: 12/05/2018
ms.keywords: _ldap_ber_skip_tag, ber_skip_tag, ber_skip_tag function [LDAP], ldap.ber__skip__tag, ldap.ber_skip_tag, winber/ber_skip_tag
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
 - ber_skip_tag
 - winber/ber_skip_tag
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
 - ber_skip_tag
---

# ber_skip_tag function


## -description

The <b>ber_skip_tag</b> function skips  the current tag and returns the tag of the next element in the supplied <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

## -parameters

### -param pBerElement [in]

Pointer to the source <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param pLen [out]

Returns the length of the skipped element.

## -returns

Returns the tag of the next element in the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to read.

## -remarks

This function is similar to 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_peek_tag">ber_peek_tag</a>, except that the state pointer, in the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> argument, is advanced past the first tag and length, and is pointed to the value part of the next element. This routine should only be used with constructed types and situations when a BER encoding is used as the value of an OCTET STRING.

## -see-also

<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_first_element">ber_first_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_next_element">ber_next_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_peek_tag">ber_peek_tag</a>