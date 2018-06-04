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

# ldap_parse_result function


## -description


The <b>ldap_parse_result</b> function parses responses from the server and returns the appropriate fields.


## -parameters




### -param Connection [in]

The session handle.


### -param ResultMessage [in]

The result of an LDAP operation as returned by one of the synchronous operation calls or by 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> for an asynchronous operation.


### -param OPTIONAL

TBD


### -param Freeit [in]

Determines whether the <i>ResultMessage</i> parameter is freed. You can pass any nonzero value to the <i>Freeit</i> parameter to free the <i>ResultMessage</i> pointer when it is no longer needed, or you can call 
<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a> to free the result later.


#### - ErrorMessage [out, optional]

A pointer to a wide, null-terminated string that contains the contents of the error message field from the <i>ResultMessage</i> parameter. Pass <b>NULL</b> to ignore this field.


#### - MatchedDNs [out, optional]

A pointer to a wide, null-terminated string. In the case of a return of <b>LDAP_NO_SUCH_OBJECT</b>, this result parameter is filled in with a distinguished name indicating how much of the name in the request was recognized. Pass <b>NULL</b> to ignore this field.


#### - Referrals [out, optional]

A pointer to a wide, null-terminated string that contains the contents of the referrals field from the <i>ResultMessage</i> parameter, indicating zero or more alternate LDAP servers where the request should be retried. Pass <b>NULL</b> to ignore this field.


#### - ReturnCode [out, optional]

Indicates the outcome of the server operation that generated the original result message. Pass <b>NULL</b> to ignore this field.


#### - ServerControls [out, optional]

This result parameter is filled in with an allocated array of controls copied from the <i>ResultMessage</i> parameter.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_parse_result</b> function traverses a chain of server responses looking for result messages to parse. Use this function if you want to access the referrals, matching distinguished names, or server controls returned. The function skips over messages of type <b>LDAP_RES_SEARCH_ENTRY</b> and <b>LDAP_RES_SEARCH_REFERENCE</b>.

When they are no longer needed, free the <i>ErrorMessage</i> and <i>MatchedDNs</i> strings by calling 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>. Free the <i>Referrals</i> array by calling 
<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>. Free the <i>ServerControls</i> by calling 
<a href="https://msdn.microsoft.com/e1e4545f-6184-41bb-bba1-4eebae9cdaaf">ldap_controls_free</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/e1e4545f-6184-41bb-bba1-4eebae9cdaaf">ldap_controls_free</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>
 

 

