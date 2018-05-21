---
UID: NF:winldap.LdapGetLastError
title: LdapGetLastError function
author: windows-driver-content
description: The LdapGetLastError function retrieves the last error code returned by an LDAP call.
old-location: ldap\ldapgetlasterror.htm
old-project: LDAP
ms.assetid: 04bcdd90-344a-4f2d-a700-e725584e49d9
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: LdapGetLastError, LdapGetLastError function [LDAP], _ldap_ldapgetlasterror, ldap.ldapgetlasterror, winldap/LdapGetLastError
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
req.unicode-ansi: 
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
-	LdapGetLastError
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LdapGetLastError function


## -description


The <b>LdapGetLastError</b> function retrieves the last error code returned by an LDAP call.


## -parameters






## -returns



An LDAP error code.




## -remarks



The <b>LdapGetLastError</b> function returns the LDAP error code for the last LDAP operation on the thread that is calling it. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for a list of possible error codes.

Multithreading: The <b>LdapGetLastError</b> function is thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>
 

 

