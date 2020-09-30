---
UID: NF:winber.ber_next_element
title: ber_next_element function (winber.h)
description: The ber_next_element function is used along with ber_first_element to traverse a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied BerElement structure. It returns the tag and length of the next element in the constructed type.
helpviewer_keywords: ["_ldap_ber_next_element","ber_next_element","ber_next_element function [LDAP]","ldap.ber__next__element","ldap.ber_next_element","winber/ber_next_element"]
old-location: ldap\ber_next_element.htm
tech.root: ldap
ms.assetid: 3daf33c9-730d-4032-a0fc-21de4c425209
ms.date: 12/05/2018
ms.keywords: _ldap_ber_next_element, ber_next_element, ber_next_element function [LDAP], ldap.ber__next__element, ldap.ber_next_element, winber/ber_next_element
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
 - ber_next_element
 - winber/ber_next_element
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
 - ber_next_element
---

# ber_next_element function


## -description

The <b>ber_next_element</b> function is used along with 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_first_element">ber_first_element</a> to traverse a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. It returns the tag and length of the next element in the constructed type.

## -parameters

### -param pBerElement [in]

Pointer to the source <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param pLen [in, out]

Returns the length of the next element to be parsed.

### -param opaque [in, out]

An opaque cookie used internally that was returned by the initial call to the 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_first_element">ber_first_element</a> function.

## -returns

Returns the tag of the next element to be read in the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.

## -remarks

The <i>pLen</i> and <i>opaque</i> pointer values returned by the function are internal parsing state values, and should not be used by applications other than as arguments to subsequent calls of this function.

## -see-also

<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_first_element">ber_first_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_peek_tag">ber_peek_tag</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_skip_tag">ber_skip_tag</a>