---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>



<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>



<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>
 

 

