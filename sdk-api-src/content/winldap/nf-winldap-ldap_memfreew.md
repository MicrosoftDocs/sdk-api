---
UID: NF:winldap.ldap_memfreeW
title: ldap_memfreeW function (winldap.h)
description: The ldap_memfreeW (Unicode) function (winldap.h) frees memory allocated from the LDAP heap.  
helpviewer_keywords: ["_ldap_ldap_memfree", "ldap.ldap__memfree", "ldap.ldap_memfree", "ldap_memfree", "ldap_memfree function [LDAP]", "ldap_memfreeW", "winldap/ldap_memfree", "winldap/ldap_memfreeW"]
old-location: ldap\ldap_memfree.htm
tech.root: ldap
ms.assetid: 3256a202-4245-4bea-a66c-0f28bfe2ef7e
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_memfree, ldap.ldap__memfree, ldap.ldap_memfree, ldap_memfree, ldap_memfree function [LDAP], ldap_memfreeA, ldap_memfreeW, winldap/ldap_memfree, winldap/ldap_memfreeA, winldap/ldap_memfreeW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_memfreeW (Unicode) and ldap_memfreeA (ANSI)
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
 - ldap_memfreeW
 - winldap/ldap_memfreeW
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
 - ldap_memfree
 - ldap_memfreeA
 - ldap_memfreeW
---

# ldap_memfreeW function


## -description

The <b>ldap_memfree</b> function frees memory allocated from the LDAP heap.

## -parameters

### -param Block [in]

A pointer to a null-terminated string that contains a pointer to memory allocated by the LDAP library.

## -returns

None.

## -remarks

Call <b>ldap_memfree</b> to free strings, such as the attribute names returned by <b>ldap_*_attribute</b>, or distinguished names returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_dn">ldap_get_dn</a>. Do not free the static buffers used by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>, and others.





> [!NOTE]
> The winldap.h header defines ldap_memfree as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_dn">ldap_get_dn</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>
