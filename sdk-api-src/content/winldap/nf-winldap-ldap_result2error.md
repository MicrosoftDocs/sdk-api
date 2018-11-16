---
UID: NF:winldap.ldap_result2error
title: ldap_result2error function
author: windows-sdk-content
description: The ldap_result2error function parses a message and returns the error code.
old-location: ldap\ldap_result2error.htm
tech.root: LDAP
ms.assetid: 67198ed0-c210-4eb1-b0f9-13cdb128c57d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_ldap_ldap_result2error, ldap.ldap__result2error, ldap.ldap_result2error, ldap_result2error, ldap_result2error function [LDAP], winldap/ldap_result2error"
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
 - ldap_result2error
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_result2error
: 
---

# ldap_result2error function


## -description


The <b>ldap_result2error</b> function parses a message and returns the error code.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The result of an LDAP operation, as returned by 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>, or one of the synchronous API operation calls.


### -param freeit [in]

Determines whether the <a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>, pointed to by the <i>res</i> parameter, is freed. Setting <i>freeit</i> to <b>TRUE</b> frees the message by calling the 
<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a> function.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Multithreading: Calls to <b>ldap_result2error</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

