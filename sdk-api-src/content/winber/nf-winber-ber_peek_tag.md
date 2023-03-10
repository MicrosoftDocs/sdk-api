---
UID: NF:winber.ber_peek_tag
title: ber_peek_tag function (winber.h)
description: Returns the tag of the next element to be parsed in the supplied BerElement structure.
helpviewer_keywords: ["_ldap_ber_peek_tag","ber_peek_tag","ber_peek_tag function [LDAP]","ldap.ber__peek__tag","ldap.ber_peek_tag","winber/ber_peek_tag"]
old-location: ldap\ber_peek_tag.htm
tech.root: ldap
ms.assetid: 0c6f24fa-47df-401c-afe8-84bf2987dd36
ms.date: 12/05/2018
ms.keywords: _ldap_ber_peek_tag, ber_peek_tag, ber_peek_tag function [LDAP], ldap.ber__peek__tag, ldap.ber_peek_tag, winber/ber_peek_tag
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
 - ber_peek_tag
 - winber/ber_peek_tag
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
 - ber_peek_tag
---

# ber_peek_tag function


## -description

The <b>ber_peek_tag</b> function returns the tag of the next element to be parsed in the supplied <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

## -parameters

### -param pBerElement [in]

Pointer to the source <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param pLen [out]

Returns the length of the next element to be parsed.

## -returns

Returns the tag of the next element to be read in the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.

## -remarks

The decoding position within the <i>pBerElement</i> parameter is unchanged by this call; that is, the fact that <b>ber_peek_tag</b> has been called does not affect future use of the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_first_element">ber_first_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_next_element">ber_next_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_skip_tag">ber_skip_tag</a>