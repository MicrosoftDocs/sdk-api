---
UID: NF:winber.ber_first_element
title: ber_first_element function (winber.h)
description: The ber_first_element function is used to begin the traversal of a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied BerElement structure. It returns the tag and length of the first element.
helpviewer_keywords: ["_ldap_ber_first_element","ber_first_element","ber_first_element function [LDAP]","ldap.ber__first__element","ldap.ber_first_element","winber/ber_first_element"]
old-location: ldap\ber_first_element.htm
tech.root: ldap
ms.assetid: 079ac0a6-1b73-433e-88b3-1ce16ddc2851
ms.date: 12/05/2018
ms.keywords: _ldap_ber_first_element, ber_first_element, ber_first_element function [LDAP], ldap.ber__first__element, ldap.ber_first_element, winber/ber_first_element
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
 - ber_first_element
 - winber/ber_first_element
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
 - ber_first_element
---

# ber_first_element function


## -description

The <b>ber_first_element</b> function is used to begin the traversal of a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. It returns the tag and length of the first element.

## -parameters

### -param pBerElement [in]

Pointer to the source <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param pLen [out]

Returns the length of the next element to be parsed.

### -param ppOpaque [out]

Returns a pointer to a cookie that is passed to subsequent calls of the 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_next_element">ber_next_element</a> function.

## -returns

Returns the tag of the next element to be read in the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.

## -remarks

The <i>pLen</i> and <i>ppOpaque</i> values returned by the function are internal parsing state values, and should not be used by applications other than as arguments to <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_next_element">ber_next_element</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_next_element">ber_next_element</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_peek_tag">ber_peek_tag</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_skip_tag">ber_skip_tag</a>