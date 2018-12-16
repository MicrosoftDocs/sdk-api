---
UID: NF:winldap.ldap_ufn2dnW
title: ldap_ufn2dnW function
author: windows-sdk-content
description: Converts a user-friendly name to a distinguished name.
old-location: ldap\ldap_ufn2dn.htm
tech.root: ldap
ms.assetid: aca3942b-4371-48d2-8975-8d184abd1a49
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_ufn2dn, ldap.ldap__ufn2dn, ldap.ldap_ufn2dn, ldap_ufn2dn, ldap_ufn2dn function [LDAP], ldap_ufn2dnA, ldap_ufn2dnW, winldap/ldap_ufn2dn, winldap/ldap_ufn2dnA, winldap/ldap_ufn2dnW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_ufn2dnW (Unicode) and ldap_ufn2dnA (ANSI)
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
 - ldap_ufn2dn
 - ldap_ufn2dnA
 - ldap_ufn2dnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_ufn2dnW function


## -description


The <b>ldap_ufn2dn</b> function converts a user-friendly name to a distinguished name.


## -parameters




### -param ufn [in]

Pointer to a null-terminated string that contains the user-friendly name to convert.


### -param pDn [out]

Pointer to a variable that receives a pointer to a null-terminated string that contains the resulting distinguished name.

If the <i>pDn</i> parameter returns non-<b>NULL</b>, free it with a call to 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_ufn2dn</b> function attempts to normalize a user-specified name to a distinguished name. For example, consider an LDAP directory format for a common name of <i>LastName</i><b>, </b><i>FirstName</i>. Given a directory name of "Jeff Smith," <b>ldap_ufn2dn</b> will attempt to normalize this to "Smith, Jeff." The function follows RFC 1781; add CN= if not present, add OU= if none present, and so on. If it runs into any errors while normalizing, the function returns a copy of what was passed. It then allocates the output string from the LDAP memory pool.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>
 

 

