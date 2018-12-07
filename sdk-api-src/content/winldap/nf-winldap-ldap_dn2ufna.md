---
UID: NF:winldap.ldap_dn2ufnA
title: ldap_dn2ufnA function
author: windows-sdk-content
description: Converts a distinguished name to a user-friendly format.
old-location: ldap\ldap_dn2ufn.htm
tech.root: ldap
ms.assetid: 6c9c943f-304a-496c-bac4-283b6c717774
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_dn2ufn, ldap.ldap__dn2ufn, ldap.ldap_dn2ufn, ldap_dn2ufn, ldap_dn2ufn function [LDAP], ldap_dn2ufnA, ldap_dn2ufnW, winldap/ldap_dn2ufn, winldap/ldap_dn2ufnA, winldap/ldap_dn2ufnW"
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
req.unicode-ansi: ldap_dn2ufnW (Unicode) and ldap_dn2ufnA (ANSI)
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
 - ldap_dn2ufn
 - ldap_dn2ufnA
 - ldap_dn2ufnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_dn2ufnA function


## -description


The <b>ldap_dn2ufn</b> function converts a distinguished name to a user-friendly format.


## -parameters




### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name to convert.


## -returns



If the function is successful, the user-friendly name is returned as a pointer to a null-terminated character string.

If the function fails, <b>NULL</b> is returned.




## -remarks



When given an entry distinguished name, <b>ldap_dn2ufn</b> returns a null-terminated character string that contains the entry name in a user-friendly format. The composition of the user-friendly format is based on the format described in RFC 1781, and depends upon the directory service implementation and the type of entry. The return value remains in memory-allocated space until you call 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>
 

 

