---
UID: NF:winldap.ldap_first_attributeW
title: ldap_first_attributeW function (winldap.h)
author: windows-sdk-content
description: Returns the first attribute.
old-location: ldap\ldap_first_attribute.htm
tech.root: ldap
ms.assetid: 2a654ef4-519f-41a7-943e-3befe5c932e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_first_attribute, ldap.ldap__first__attribute, ldap.ldap_first_attribute, ldap_first_attribute, ldap_first_attribute function [LDAP], ldap_first_attributeA, ldap_first_attributeW, winldap/ldap_first_attribute, winldap/ldap_first_attributeA, winldap/ldap_first_attributeW"
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_first_attributeW function


## -description


For a given directory entry, the <b>ldap_first_attribute</b> function returns the first attribute.


## -parameters




### -param ld [in]

The session handle.


### -param entry [in]

The entry whose attributes are to be stepped through, as returned by 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a> or 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>.


### -param ptr [out]

The address of a pointer used internally to track the current position in the entry.


## -returns



A pointer to a null-terminated string. If the function succeeds, it returns a pointer to an allocated buffer that contains the current attribute name. When there are no more attributes to step through, it returns <b>NULL</b>. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and sets the session error parameter in the LDAP data structure to the LDAP error code.




## -remarks



Use 
<b>ldap_first_attribute</b> in conjunction with 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a> to step through the list of attribute types returned with an entry. You can then pass these attribute names in a call to 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a> to retrieve their associated values.

A call to 
<b>ldap_first_attribute</b> allocates, and returns through the <i>ptr</i> parameter, a pointer to a 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. Pass this pointer to 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a> to track the current position in the list of attributes. When you have finished stepping through a list of attributes and <i>ptr</i> is non-<b>NULL</b>, free the pointer by calling 
<a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a>( ptr, 0 ). Be aware that you must pass the second parameter as 0 (zero) in this call.

Both 
<b>ldap_first_attribute</b> and 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a> return a pointer to an allocated buffer containing the current attribute name. Free this buffer, when no longer required, by calling 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>. Because this buffer is overwritten on the next call to either 
<b>ldap_first_attribute</b> or  
<b>ldap_next_attribute</b>, the user should make a copy of the attribute name if it must be preserved for processing.




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>



<a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>
 

 

