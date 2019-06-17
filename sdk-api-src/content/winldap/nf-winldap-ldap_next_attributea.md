---
UID: NF:winldap.ldap_next_attributeA
title: ldap_next_attributeA function (winldap.h)
author: windows-sdk-content
description: Returns the next attribute.
old-location: ldap\ldap_next_attribute.htm
tech.root: ldap
ms.assetid: 4df50d80-0d01-4d7f-b542-865b84bac2a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_next_attribute, ldap.ldap__next__attribute, ldap.ldap_next_attribute, ldap_next_attribute, ldap_next_attribute function [LDAP], ldap_next_attributeA, ldap_next_attributeW, winldap/ldap_next_attribute, winldap/ldap_next_attributeA, winldap/ldap_next_attributeW"
ms.topic: function
f1_keywords: ["winldap/ldap_next_attribute"]
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_next_attributeW (Unicode) and ldap_next_attributeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_next_attribute
 - ldap_next_attributeA
 - ldap_next_attributeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_next_attributeA function


## -description


For a given entry, the <b>ldap_next_attribute</b> function returns the next attribute.


## -parameters




### -param ld [in]

The session handle.


### -param entry [in]

The entry whose attributes are to be stepped through, as returned by 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a> or 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>.


### -param ptr [in, out]

The address of a pointer used internally to track the current position in the entry.


## -returns



If the function succeeds, it returns a pointer to a null-terminated string that contains the current attribute name. If there are no more attributes to step through, it returns <b>NULL</b>. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and sets the session error parameter in the LDAP data structure to the LDAP error code.




## -remarks



Use 
<b>ldap_next_attribute</b> in conjunction with 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a> to step through the list of attribute types returned with an entry. You can then pass these attribute names in a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a> to retrieve their associated values.

A call to 
<b>ldap_next_attribute</b> returns, through the <i>ptr</i> parameter, a pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure. Pass this pointer to the next call to 
<b>ldap_next_attribute</b> to track the current position in the list of attributes. When you have finished stepping through a list of attributes, and <i>ptr</i> is non-<b>NULL</b>, free the pointer by calling 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a> (ptr, 0). Be aware that you must pass the second parameter as 0 (zero) in this call.

The 
<b>ldap_next_attribute</b> function returns a pointer to an internally  allocated buffer that contains the current attribute name. Free this buffer, when no longer required, by calling 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>. Because this buffer is overwritten on the next call to either 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a> or 
<b>ldap_next_attribute</b>, the user should make a copy of the attribute name if it must be preserved for processing.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_attribute">ldap_first_attribute</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>
 

 

