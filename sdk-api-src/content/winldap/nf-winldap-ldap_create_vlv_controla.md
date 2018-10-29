---
UID: NF:winldap.ldap_create_vlv_controlA
title: ldap_create_vlv_controlA function
author: windows-sdk-content
description: The ldap_create_vlv_control function is used to create the request control (LDAP_CONTROL_VLVREQUEST) on the server.
old-location: ldap\ldap_create_vlv_control.htm
tech.root: LDAP
ms.assetid: f4305aa9-e967-45a8-8b8b-49b1e60994e8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_ldap_ldap_create_vlv_control, ldap.ldap__create__vlv__control, ldap.ldap_create_vlv_control, ldap_create_vlv_control, ldap_create_vlv_control function [LDAP], ldap_create_vlv_controlA, ldap_create_vlv_controlW, winldap/ldap_create_vlv_control, winldap/ldap_create_vlv_controlA, winldap/ldap_create_vlv_controlW"
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
req.unicode-ansi: ldap_create_vlv_controlW (Unicode) and ldap_create_vlv_controlA (ANSI)
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
 - ldap_create_vlv_control
 - ldap_create_vlv_controlA
 - ldap_create_vlv_controlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_create_vlv_controlA function


## -description


The <b>ldap_create_vlv_control</b> function is used to create the request control (<a href="https://msdn.microsoft.com/9f00ca19-544e-4616-a70a-e7e62fa84f53">LDAP_CONTROL_VLVREQUEST</a>) on the server.


## -parameters




### -param ExternalHandle [in]

An LDAP session handle, as obtained from a call to <a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>.


### -param VlvInfo [in]

The address of an <a href="https://msdn.microsoft.com/2018ecb1-9b32-4afa-ad20-5cdae396376d">LDAPVLVInfo</a> structure whose contents are used to construct the value of the control created.


### -param IsCritical [in]

If this value is not zero, the control created will have its criticality set to <b>TRUE</b>.


### -param Control [out]

A result parameter assigned the address of an <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structure that contains the request control (<a href="https://msdn.microsoft.com/9f00ca19-544e-4616-a70a-e7e62fa84f53">LDAP_CONTROL_VLVREQUEST</a>) created by this function.


## -returns



The <b>ldap_create_vlv_control</b> function returns an 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">LDAP error code</a> to indicate failure, or LDAP_SUCCESS if successful.




## -remarks



When a VLV search is conducted, the client must use this function to create a new VLV control that can be included in the search request sent to the server. The server will assign a contextID for this VLV search, passed to the client. When the VLV search is completed, you should use <a href="https://msdn.microsoft.com/10729355-8f80-477b-acc8-705db72cebdb">ldap_control_free</a> to free the control returned by <b>ldap_create_vlv_control</b>, and <a href="https://msdn.microsoft.com/e1e4545f-6184-41bb-bba1-4eebae9cdaaf">ldap_controls_free</a> to free the  array of controls, including the VLV response control, returned by <a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>.

For more information, and  a code example for this function, see 
<a href="https://msdn.microsoft.com/d4c4f5ca-13a2-45f6-8b4f-2ff0cb67eb8d">Example Code for Using LDAP VLV</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a>



<a href="https://msdn.microsoft.com/2018ecb1-9b32-4afa-ad20-5cdae396376d">LDAPVLVInfo</a>



<a href="https://msdn.microsoft.com/9f00ca19-544e-4616-a70a-e7e62fa84f53">LDAP_CONTROL_VLVREQUEST</a>



<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>



<a href="https://msdn.microsoft.com/b2b03021-7e6a-413b-8e0a-df037d9a71de">Searching with the LDAP VLV Control</a>



<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a>



<a href="https://msdn.microsoft.com/a1a1e47f-c53b-48a3-9c40-0e1518c5c729">ldap_parse_vlv_control</a>



<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>
 

 

