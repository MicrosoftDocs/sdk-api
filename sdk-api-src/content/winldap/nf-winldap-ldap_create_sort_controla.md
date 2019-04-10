---
UID: NF:winldap.ldap_create_sort_controlA
title: ldap_create_sort_controlA function (winldap.h)
author: windows-sdk-content
description: The ldap_create_sort_control function is used to format a list of sort keys into a search control. Support for controls is available effective with LDAP 3, but whether the sort control is supported or not is dependent on the particular server.
old-location: ldap\ldap_create_sort_control.htm
tech.root: ldap
ms.assetid: bbf8f860-ead8-4b22-8efa-0697076267ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_create_sort_control, ldap.ldap__create__sort__control, ldap.ldap_create_sort_control, ldap_create_sort_control, ldap_create_sort_control function [LDAP], ldap_create_sort_controlA, ldap_create_sort_controlW, winldap/ldap_create_sort_control, winldap/ldap_create_sort_controlA, winldap/ldap_create_sort_controlW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_create_sort_controlW (Unicode) and ldap_create_sort_controlA (ANSI)
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
 - ldap_create_sort_control
 - ldap_create_sort_controlA
 - ldap_create_sort_controlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_create_sort_controlA function


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




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a>



<a href="https://msdn.microsoft.com/03c51778-45ed-46de-94a2-425bf7030cf0">LDAP_SERVER_SORT_OID</a>



<a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a>
 

 

