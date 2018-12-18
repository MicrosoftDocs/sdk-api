---
UID: NF:winldap.ldap_get_dnW
title: ldap_get_dnW function
author: windows-sdk-content
description: The ldap_get_dn function retrieves the distinguished name for a given entry.
old-location: ldap\ldap_get_dn.htm
tech.root: ldap
ms.assetid: 00484fe7-65d2-4300-ab5c-0a69a25e65e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_get_dn, ldap.ldap__get__dn, ldap.ldap_get_dn, ldap_get_dn, ldap_get_dn function [LDAP], ldap_get_dnA, ldap_get_dnW, winldap/ldap_get_dn, winldap/ldap_get_dnA, winldap/ldap_get_dnW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_dnW (Unicode) and ldap_get_dnA (ANSI)
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
 - ldap_get_dn
 - ldap_get_dnA
 - ldap_get_dnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_get_dnW function


## -description


The <b>ldap_get_dn</b> function retrieves the distinguished name for a given entry.


## -parameters




### -param ld [in]

The session handle.


### -param entry [in]

The entry whose distinguished name is to be retrieved.


## -returns



If the function succeeds, it returns the distinguished name as a pointer to a null-terminated character string.

If the function fails, it returns <b>NULL</b> and sets the session error parameters in the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> data structure.




## -remarks



The <b>ldap_get_dn</b> function retrieves the distinguished name for an entry that was returned by 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>, or 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>. When the returned name is no longer needed, free the string by calling 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>
 

 

