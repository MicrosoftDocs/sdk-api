---
UID: NF:winldap.ldap_create_page_control
title: ldap_create_page_control function
author: windows-driver-content
description: Use the ldap_create_page_control function to create a basic control for paging results. Support for controls is available effective with LDAP 3, but whether the page control is supported or not is dependent on the particular server.
old-location: ldap\ldap_create_page_control.htm
old-project: LDAP
ms.assetid: b3b1f3bd-7eb3-4f76-921c-386562dae2e2
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: "_ldap_ldap_create_page_control, ldap.ldap__create__page__control, ldap.ldap_create_page_control, ldap_create_page_control, ldap_create_page_control function [LDAP], ldap_create_page_controlA, ldap_create_page_controlW, winldap/ldap_create_page_control, winldap/ldap_create_page_controlA, winldap/ldap_create_page_controlW"
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
req.unicode-ansi: ldap_create_page_controlW (Unicode) and ldap_create_page_controlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_create_page_control
-	ldap_create_page_controlA
-	ldap_create_page_controlW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_create_page_control function


## -description


Use the <b>ldap_create_page_control</b> function to create a basic control for paging results. Support for controls is available effective with LDAP 3, but whether the page control is supported or not is dependent on the particular server.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param PageSize [in]

The number of entries to return in each page.


### -param Cookie [in]

Pointer to a 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure that the server uses to determine its location in the result set. This is an opaque structure that you should not access directly. Set to <b>NULL</b> for the first call to <b>ldap_create_page_control</b>.


### -param IsCritical [in]

Notifies the server whether this control is critical to the search.


### -param Control [out]

Pointer to the newly created control.


## -returns



This function returns WINLDAPAPI ULONG LDAPAPI.




## -remarks



The <b>ldap_create_page_control</b> function creates a simple paged-results control. The control enables the client to specify the rate at which an LDAP server returns the results of a search operation. This is useful when the client has limited resources and may not be able to process the entire result set from a given LDAP query, or when the client/server connection is slow.

To create the paged-results control, specify the number of entries to be returned in a single page. To return results normally, even if it cannot support this control, set the <i>IsCritical</i> parameter to <b>FALSE</b>.

This function creates the control - it does not verify that the server supports it, and consequently, does not return <b>LDAP_UNAVAILABLE_CRIT_EXTENSION</b> if the server does not support the control. However, it can return other standard LDAP return values, such as <b>LDAP_NO_MEMORY</b> or <b>LDAP_PARAM_ERROR</b>.

When <b>ldap_create_page_control</b> returns successfully, include the newly created control to the list of server controls in a call to 
<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a> or to 
<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>. When the server returns the first page of results, call 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a> to retrieve the first page of results.

Call 
<a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a> when the control is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/bd896700-70a9-4568-9f54-8ab56d0eacd8">LDAP_PAGED_RESULT_OID_STRING</a>



<a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a>



<a href="https://msdn.microsoft.com/babf74d1-2f9c-40f8-ba82-e298e49ad937">ldap_parse_page_control</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>



<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>
 

 

