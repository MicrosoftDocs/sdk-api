---
UID: NF:winldap.ldap_first_attributeW
title: ldap_first_attributeW function (winldap.h)
description: The ldap_first_attributeW (Unicode) function (winldap.h) returns the first attribute.
helpviewer_keywords: ["_ldap_ldap_first_attribute", "ldap.ldap__first__attribute", "ldap.ldap_first_attribute", "ldap_first_attribute", "ldap_first_attribute function [LDAP]", "ldap_first_attributeW", "winldap/ldap_first_attribute", "winldap/ldap_first_attributeW"]
old-location: ldap\ldap_first_attribute.htm
tech.root: ldap
ms.assetid: 2a654ef4-519f-41a7-943e-3befe5c932e8
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_first_attribute, ldap.ldap__first__attribute, ldap.ldap_first_attribute, ldap_first_attribute, ldap_first_attribute function [LDAP], ldap_first_attributeA, ldap_first_attributeW, winldap/ldap_first_attribute, winldap/ldap_first_attributeA, winldap/ldap_first_attributeW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_first_attributeW (Unicode) and ldap_first_attributeA (ANSI)
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
 - ldap_first_attributeW
 - winldap/ldap_first_attributeW
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
 - ldap_first_attribute
 - ldap_first_attributeA
 - ldap_first_attributeW
---

# ldap_first_attributeW function


## -description

For a given directory entry, the <b>ldap_first_attribute</b> function returns the first attribute.

## -parameters

### -param ld [in]

The session handle.

### -param entry [in]

The entry whose attributes are to be stepped through, as returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>.

### -param ptr [out]

The address of a pointer used internally to track the current position in the entry.

## -returns

A pointer to a null-terminated string. If the function succeeds, it returns a pointer to an allocated buffer that contains the current attribute name. When there are no more attributes to step through, it returns <b>NULL</b>. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and sets the session error parameter in the LDAP data structure to the LDAP error code.

## -remarks

Use 
<b>ldap_first_attribute</b> in conjunction with 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a> to step through the list of attribute types returned with an entry. You can then pass these attribute names in a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a> to retrieve their associated values.

A call to 
<b>ldap_first_attribute</b> allocates, and returns through the <i>ptr</i> parameter, a pointer to a 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. Pass this pointer to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a> to track the current position in the list of attributes. When you have finished stepping through a list of attributes and <i>ptr</i> is non-<b>NULL</b>, free the pointer by calling 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a>( ptr, 0 ). Be aware that you must pass the second parameter as 0 (zero) in this call.

Both 
<b>ldap_first_attribute</b> and 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a> return a pointer to an allocated buffer containing the current attribute name. Free this buffer, when no longer required, by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>. Because this buffer is overwritten on the next call to either 
<b>ldap_first_attribute</b> or  
<b>ldap_next_attribute</b>, the user should make a copy of the attribute name if it must be preserved for processing.





> [!NOTE]
> The winldap.h header defines ldap_first_attribute as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_attribute">ldap_next_attribute</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>
