---
UID: NF:winldap.ldap_unbind
title: ldap_unbind function (winldap.h)
author: windows-sdk-content
description: The ldap_unbind function frees resources associated with an LDAP session.
old-location: ldap\ldap_unbind.htm
tech.root: ldap
ms.assetid: 5d8b3198-3935-4305-b0f1-eaf1a9355cf3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_unbind, ldap.ldap__unbind, ldap.ldap_unbind, ldap_unbind, ldap_unbind function [LDAP], winldap/ldap_unbind"
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
 - ldap_unbind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_unbind function


## -description


The <b>ldap_unbind</b> function frees resources associated with an LDAP session.


## -parameters




### -param ld [in]

The session handle.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_unbind</b> to unbind from the directory, close the connection, and dispose of the session handle. Call this function when you have finished with an <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> connection structure, even if you have not called 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> when opening the connection. Ensure that you do not inadvertently call this function more than once on a session handle because doing so can free resources that you did not intend to release.

The <b>ldap_unbind</b> function is for the asynchronous set of APIs, but it completes synchronously. There is no server response to an unbind operation.

Multithreading: Calls to <b>ldap_unbind</b> are safe, but you cannot use the session handle to the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> structure after it has been freed.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/b4dcf3cc-d4cb-40ca-a57e-150d4008108c">ldap_unbind_s</a>
 

 

