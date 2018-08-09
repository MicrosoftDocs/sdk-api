---
UID: NF:winldap.ldap_parse_sort_controlW
title: ldap_parse_sort_controlW function
author: windows-sdk-content
description: The ldap_parse_sort_control function parses the sort control returned by the server.
old-location: ldap\ldap_parse_sort_control.htm
old-project: ldap
ms.assetid: 71d6bae2-3ee4-417c-8c1b-d277cad03f36
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_parse_sort_control, ldap.ldap__parse__sort__control, ldap.ldap_parse_sort_control, ldap_parse_sort_control, ldap_parse_sort_control function [LDAP], ldap_parse_sort_controlA, ldap_parse_sort_controlW, winldap/ldap_parse_sort_control, winldap/ldap_parse_sort_controlA, winldap/ldap_parse_sort_controlW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_sort_controlW (Unicode) and ldap_parse_sort_controlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_parse_sort_control
 - ldap_parse_sort_controlA
 - ldap_parse_sort_controlW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_parse_sort_controlW function


## -description


The <b>ldap_parse_sort_control</b> function parses the sort control returned by the server.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param Control [in]

The control returned from the server, as obtained from a call to 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>.


### -param Result [out]

The result code.


### -param Attribute [out]

A pointer to a null-terminated string that contains the name of the attribute that caused the operation to fail.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



When the server returns the results, it returns a control in the SearchResultDone message. Call <b>ldap_parse_sort_control</b> to parse this sort control.

If the sort operation failed, the server may return the name of the attribute that caused the failure. In this case, call 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> to free the attribute value




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>
 

 

