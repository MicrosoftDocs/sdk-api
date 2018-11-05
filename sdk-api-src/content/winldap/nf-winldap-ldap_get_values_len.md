---
UID: NF:winldap.ldap_get_values_len
title: ldap_get_values_len function
author: windows-sdk-content
description: The ldap_get_values_len function retrieves the list of values for a given attribute.
old-location: ldap\ldap_get_values_len.htm
tech.root: ldap
ms.assetid: e2100892-5dad-4fc7-8129-34c675bcf134
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ldap_ldap_get_values_len, ldap.ldap__get__values__len, ldap.ldap_get_values_len, ldap_get_values_len, ldap_get_values_len function [LDAP], ldap_get_values_lenA, ldap_get_values_lenW, winldap/ldap_get_values_len, winldap/ldap_get_values_lenA, winldap/ldap_get_values_lenW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_values_lenW (Unicode) and ldap_get_values_lenA (ANSI)
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
 - ldap_get_values_len
 - ldap_get_values_lenA
 - ldap_get_values_lenW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_get_values_len function


## -description


The <b>ldap_get_values_len</b> function retrieves the list of values for a given attribute.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param Message [in]

Handle to the 
<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a> structure.


### -param attr [in]

A pointer to a null-terminated string that contains the attribute whose values are to be retrieved.


## -returns



If the function succeeds, it returns a null-terminated list of pointers to 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures that contain the values of the specified attribute. If no attribute values were found, it returns <b>NULL</b>. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and the session error parameter in the LDAP data structure is set to the LDAP error code.




## -remarks



Use <b>ldap_get_values_len</b> when parsing a search response to obtain the value or values of an attribute. Use this function when the attribute contains binary data; for attributes whose values are null-terminated character strings, use 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>.

The entry is obtained by calling 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a> or 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>. The attribute should be one returned by a call to 
<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>, 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>, or a caller-supplied string (for example, "mail").

Call 
<a href="https://msdn.microsoft.com/bae95e09-bb3b-4fb3-887f-3cff0a0e6c22">ldap_value_free_len</a> to release the returned value when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>



<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/bae95e09-bb3b-4fb3-887f-3cff0a0e6c22">ldap_value_free_len</a>
 

 

