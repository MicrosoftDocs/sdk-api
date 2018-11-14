---
UID: NF:winldap.ldap_conn_from_msg
title: ldap_conn_from_msg function
author: windows-sdk-content
description: Returns the LDAP session handle (connection pointer) for a particular message.
old-location: ldap\ldap_conn_from_msg.htm
tech.root: ldap
ms.assetid: 0f536c42-06c1-43d9-a298-4a9e9bf96a46
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ldap_ldap_conn_from_msg, ldap.ldap__conn__from__msg, ldap.ldap_conn_from_msg, ldap_conn_from_msg, ldap_conn_from_msg function [LDAP], winldap/ldap_conn_from_msg"
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
 - ldap_conn_from_msg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_conn_from_msg
: 
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



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>



<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">structures</a>
 

 

