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

# ldap_create_sort_controlW function


## -description


The <b>ldap_create_sort_control</b> function is used to format a list of sort keys into a search control. Support for controls is available effective with LDAP 3, but whether the sort control is supported or not is dependent on the particular server.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param SortKeys [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a> structures. Each structure in the array specifies the name of an attribute to use as a sort key, the matching rule for that key, and whether the sort order is ascending or descending.


### -param IsCritical [in]

Notifies the server whether this control is critical to the search. 0 ==&gt; FALSE, !0 ==&gt; TRUE.


### -param Control [out]

Pointer to the newly created control.


## -returns



This function returns WINLDAPAPI ULONG LDAPAPI.




## -remarks



The <b>ldap_create_sort_control</b> function creates a basic sort control. Such a control is useful when the LDAP client has limited functionality and cannot sort results, yet needs them sorted.

The sort controls allow a server to return a result code for the sorting of the results that is independent of the result code returned for the search operation.

This function creates the control — it does not verify that  the server supports it, and consequently, does not return LDAP_UNAVAILABLE_CRIT_EXTENSION if the server does not support the control. However, it can return other standard LDAP return values, such as LDAP_NO_MEMORY or LDAP_PARAM_ERROR.

To free the control when it is no longer required, call 
<a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a>



<a href="https://msdn.microsoft.com/03c51778-45ed-46de-94a2-425bf7030cf0">LDAP_SERVER_SORT_OID</a>



<a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a>
 

 

