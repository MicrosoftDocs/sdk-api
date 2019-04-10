---
UID: NF:winldap.ldap_encode_sort_control
title: ldap_encode_sort_control function (winldap.h)
author: windows-sdk-content
description: The ldap_encode_sort_control function formats a list of sort keys into a search control. This function is obsolete. Instead, use ldap_create_sort_control.
old-location: ldap\ldap_encode_sort_control.htm
tech.root: ldap
ms.assetid: 5c6c3bd4-739f-413d-adc3-668ac7b56da6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_encode_sort_control, ldap.ldap__encode__sort__control, ldap.ldap_encode_sort_control, ldap_encode_sort_control, ldap_encode_sort_control function [LDAP], ldap_encode_sort_controlA, ldap_encode_sort_controlW, winldap/ldap_encode_sort_control, winldap/ldap_encode_sort_controlA, winldap/ldap_encode_sort_controlW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_encode_sort_controlW (Unicode) and ldap_encode_sort_controlA (ANSI)
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
 - ldap_encode_sort_control
 - ldap_encode_sort_controlA
 - ldap_encode_sort_controlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_encode_sort_control function


## -description


The <b>ldap_encode_sort_control</b> function formats a list of sort keys into a search control. This function is obsolete. Instead, use 
<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a>.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param SortKeys [in]

A list of 
<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a> structures.


### -param Control [out]

Pointer to the new control.


### -param Criticality [in]

Notifies the server whether this control is critical to the search.


## -returns



If the call completed successfully, <b>LDAP_SUCCESS</b> is returned. Other standard LDAP return values, such as <b>LDAP_NO_MEMORY</b> or <b>LDAP_PARAM_ERROR</b>, may also be returned.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a>



<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a>
 

 

