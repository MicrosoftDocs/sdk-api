---
UID: NF:winldap.ldap_unbind_s
title: ldap_unbind_s function
author: windows-sdk-content
description: The ldap_unbind_s function synchronously frees resources associated with an LDAP session.
old-location: ldap\ldap_unbind_s.htm
tech.root: ldap
ms.assetid: b4dcf3cc-d4cb-40ca-a57e-150d4008108c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_unbind_s, ldap.ldap__unbind__s, ldap.ldap_unbind_s, ldap_unbind_s, ldap_unbind_s function [LDAP], winldap/ldap_unbind_s"
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
 - ldap_unbind_s
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_unbind_s function


## -description


The <b>ldap_unbind_s</b> function synchronously frees resources associated with an LDAP session.


## -parameters




### -param ld [in]

The session handle.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_unbind_s</b> to unbind from the directory, close the connection, and dispose of the session handle.  Call this function when the  <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> connection structure is no longer required, even if you have not called 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> when opening the connection. Ensure that you do not inadvertently call this function more than once on a session handle because doing so can free resources that you did not intend to release.

Both 
<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> and <b>ldap_unbind_s</b> work synchronously. There is no server response to an unbind operation.

Multithreading: Calls to <b>ldap_unbind_s</b> are safe except that you cannot use the session handle to the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> structure after it has been freed.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

