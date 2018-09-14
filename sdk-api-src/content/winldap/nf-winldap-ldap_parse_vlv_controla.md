---
UID: NF:winldap.ldap_parse_vlv_controlA
title: ldap_parse_vlv_controlA function
author: windows-sdk-content
description: Used to find and parse VLV search results.
old-location: ldap\ldap_parse_vlv_control.htm
tech.root: LDAP
ms.assetid: a1a1e47f-c53b-48a3-9c40-0e1518c5c729
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "_ldap_ldap_parse_vlv_control, ldap.ldap__parse__vlv__control, ldap.ldap_parse_vlv_control, ldap_parse_vlv_control, ldap_parse_vlv_control function [LDAP], ldap_parse_vlv_controlA, ldap_parse_vlv_controlW, winldap/ldap_parse_vlv_control, winldap/ldap_parse_vlv_controlA, winldap/ldap_parse_vlv_controlW"
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
req.unicode-ansi: ldap_parse_vlv_controlW (Unicode) and ldap_parse_vlv_controlA (ANSI)
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
 - ldap_parse_vlv_control
 - ldap_parse_vlv_controlA
 - ldap_parse_vlv_controlW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_parse_vlv_controlA function


## -description


The <b>ldap_parse_vlv_control</b> function is used to find and parse VLV search results.


## -parameters




### -param ExternalHandle [in]

The LDAP session handle.


### -param Control [in]

The address of a NULL-terminated array of <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structures, typically obtained by a call to 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>.


### -param TargetPos [out]

The numeric position of the target entry in the result set list, as provided by the targetPosition element of the BER-encoded response control (<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the target position is not returned.


### -param ListCount [out]

The server estimate of the number of entries in the list as provided by the contentCount element of the BER-encoded response control (<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the size is not returned.


### -param Context [out]

The server-generated context identifier. If the server does not return a context identifier, this parameter will be set to <b>NULL</b>. If <b>NULL</b> is passed for contextp, the context identifier is not returned.


### -param ErrCode [out]

The VLV result code, as provided by the virtualListViewResult element of the BER-encoded response control (<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the result code is not returned.


## -returns



This function returns an 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">LDAP error code</a> that indicates whether a VLV result control was found and parsed successfully. <b>LDAP_SUCCESS</b> is returned if all goes well, <b>LDAP_CONTROL_MISSING</b> is returned if the <i>ctrls</i> array does not include a response control (<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>), and another LDAP error code is returned if a parsing error or other issue occurs.

VLV uses the following LDAP return value codes:

<b>LDAP_OPERATIONS_ERROR</b>

<b>LDAP_UNWILLING_TO_PERFORM</b>

<b>LDAP_INSUFFICIENT_ACCESS</b>

<b>LDAP_BUSY</b>

<b>LDAP_TIMELIMIT_EXCEEDED</b>

<b>LDAP_ADMINLIMIT_EXCEEDED</b>

<b>LDAP_OTHER</b>

In addition, the following two codes have been added to support VLV:




## -remarks



This control parses the search results returned by the server in the response control (<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>). A context identifier is passed from the server to the client to identify the control, which must be freed at the end of the session by calling 
<a href="https://msdn.microsoft.com/9e5a4bb9-568d-48ee-be75-952916c021b1">ber_bvfree</a>.

For more information and a code example, see 
<a href="https://msdn.microsoft.com/d4c4f5ca-13a2-45f6-8b4f-2ff0cb67eb8d">Example Code for Using LDAP VLV</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a>



<a href="https://msdn.microsoft.com/2018ecb1-9b32-4afa-ad20-5cdae396376d">LDAPVLVInfo</a>



<a href="https://msdn.microsoft.com/9f00ca19-544e-4616-a70a-e7e62fa84f53">LDAP_CONTROL_VLVREQUEST</a>



<a href="https://msdn.microsoft.com/bd7906bd-9e2d-4941-9a63-3e530cb9583b">LDAP_CONTROL_VLVRESPONSE</a>



<a href="https://msdn.microsoft.com/b2b03021-7e6a-413b-8e0a-df037d9a71de">Searching with the LDAP VLV Control</a>



<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a>



<a href="https://msdn.microsoft.com/f4305aa9-e967-45a8-8b8b-49b1e60994e8">ldap_create_vlv_control</a>



<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>
 

 

