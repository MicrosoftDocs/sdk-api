---
UID: NF:winldap.ldap_err2stringW
title: ldap_err2stringW function
author: windows-sdk-content
description: Converts a numeric LDAP error code into a null-terminated character string that describes the error.
old-location: ldap\ldap_err2string.htm
old-project: ldap
ms.assetid: ebdccc79-e9c7-4a25-a1ab-01ba2b6f2d59
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_err2string, ldap.ldap__err2string, ldap.ldap_err2string, ldap_err2string, ldap_err2string function [LDAP], ldap_err2stringA, ldap_err2stringW, winldap/ldap_err2string, winldap/ldap_err2stringA, winldap/ldap_err2stringW"
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
req.unicode-ansi: ldap_err2stringW (Unicode) and ldap_err2stringA (ANSI)
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
 - ldap_err2string
 - ldap_err2stringA
 - ldap_err2stringW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_err2stringW function


## -description


The <b>ldap_err2string</b> function converts a numeric LDAP error code into a null-terminated character string that describes the error.


## -parameters




### -param err [in]

An LDAP error code as returned by another LDAP function.


## -returns



If the function succeeds, a pointer to a null-terminated character string that describes the error, is returned.

If the function fails, a pointer to <b>NULL</b> is returned.




## -remarks



Call <b>ldap_err2string</b> to convert any  numeric LDAP error code into an informative, null-terminated character string message that describes the error. Be aware that some of the asynchronous calls return -1. In this case, use <a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> to retrieve the LDAP error code, and then use <b>ldap_err2string</b> on that value.

The return value is a static pointer to the character string. Do not free this string.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>
 

 

