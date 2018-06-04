---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ldap_conn_from_msg function


## -description


The <b>ldap_conn_from_msg</b> function returns the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle (connection pointer) for a particular message.


## -parameters




### -param PrimaryConn [in]

A pointer to the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle of the message, if known. If the <b>LDAP</b> session handle for the message is unknown, then <b>NULL</b> may be passed for this parameter provided that the 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option had been previously set for the message session.


### -param res [in]

The <b>LDAP</b> message queried.  If <b>NULL</b> is passed for this parameter, then the function will respond with a <b>NULL</b> return value.


## -returns




      The return value is the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle (connection pointer) where the message originated from. This function returns <b>NULL</b> if the originating session has closed or if a <b>NULL</b> <b>LDAPMessage</b> pointer is passed to the function and the <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option was not previously set for the message session.




## -remarks



This function is used to identify the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle associated with the specified <b>LDAP</b> message. It returns a valid <b>LDAP</b> session handle only if one of the following  conditions are met:

<ul>
<li>The <a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a> originated from the same <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session handle passed to the function in the <i>PrimaryConn</i> parameter.</li>
<li>The <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option was previously enabled on the <a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> session associated with the message.</li>
</ul>
If neither of these conditions are met, the function returns a <b>NULL</b> session handle.




## -see-also




<a href="https://msdn.microsoft.com/d11da030-b521-4469-9212-63800b412e68">Establishing an LDAP Session</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">structures</a>
 

 

