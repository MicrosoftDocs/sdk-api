---
UID: NF:winldap.ldap_get_values
title: ldap_get_values function (winldap.h)
author: windows-sdk-content
description: The ldap_get_values function retrieves the list of values of a given attribute.
old-location: ldap\ldap_get_values.htm
tech.root: ldap
ms.assetid: a633afa1-4a37-4894-ae94-5225d99077fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_get_values, ldap.ldap__get__values, ldap.ldap_get_values, ldap_get_values, ldap_get_values function [LDAP], ldap_get_valuesA, ldap_get_valuesW, winldap/ldap_get_values, winldap/ldap_get_valuesA, winldap/ldap_get_valuesW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_valuesW (Unicode) and ldap_get_valuesA (ANSI)
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
 - ldap_get_values
 - ldap_get_valuesA
 - ldap_get_valuesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_get_values function


## -description


The <b>ldap_get_values</b> function retrieves the list of values of a given attribute.


## -parameters




### -param ld [in]

The session handle.


### -param entry [in]

The entry from which to retrieve values.


### -param attr [in]

A pointer to a null-terminated string that contains the attribute whose values are to be retrieved.


## -returns



If the function succeeds, it returns a null-terminated list of pointers to values. If no attribute values were found, it usually returns <b>NULL</b>. But in some cases it may return a list one pointer that is <b>NULL</b>. Always make sure to use <a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a> to get the count of values in the returned list, as noted in Remarks. The session error parameter in the LDAP data structure is set to 0 in either case.

If the function fails, it returns <b>NULL</b> and the session error parameter in the LDAP data structure is set to the LDAP error code.




## -remarks



Use <b>ldap_get_values</b> when parsing a search response to obtain the value or values of an attribute. Use this function only when the attribute contains null-terminated character strings; for binary data, use 
<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a> instead.

The entry is obtained by calling 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a> or 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>. The attribute should be one returned by a call to 
<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>, 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>, or a caller-supplied string (for example, "mail").

Use <a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a> to get the count of values in the returned list.
Call 
<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a> to release the returned value when it is no longer required.

Certain LDAP servers place limits on the number of attribute string values that are returned in a single call.  For more information about using range retrieval specifiers, see <a href="https://msdn.microsoft.com/fe94299e-5c09-4744-bf2c-3bea7538d959">Searching Using Range Retrieval</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>



<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>



<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>
 

 

