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

# ldap_start_tls_sA function


## -description


The <b>ldap_start_tls_s</b> function is used in an active LDAP session to begin using TLS encryption.


## -parameters




### -param ExternalHandle [in]

A pointer to an <b>LDAP</b> structure that represents the current session.


### -param ServerReturnValue [out]

Optional. A pointer to a <b>ULONG</b> that may contain a server error code. This parameter should be consulted if <b>LDAP_OTHER</b> is returned in the return value.  Pass in <b>NULL</b> if you do not wish to use it.


### -param result [out]

Optional. A pointer to a pointer for an <a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>  structure that may contain a server referral message.  Pass in <b>NULL</b> if you do not wish to use it.


### -param ServerControls [in]

Optional. A NULL-terminated array of pointers to  <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structures that represent server controls.  Pass in <b>NULL</b> if you do not want to specify server  controls.


### -param ClientControls [in]

Optional. A NULL-terminated array of pointers to <a href="https://msdn.microsoft.com/c0b4d712-021d-46f3-8bda-aaf660ec1acc">LDAPControl</a> structures that represent client controls.  Pass in <b>NULL</b> if you do not want to specify client controls.


## -returns



If the function call succeeds, <b>LDAP_SUCCESS</b> is returned. <b>LDAP_UNWILLING_TO_PERFORM</b> is returned if a TLD/SSL session is already in progress, or if a bind is currently in progress, or if there is an outstanding LDAP request on the connection. If the server rejects the extended operation, <b>LDAP_OTHER</b> is returned and the <i>ServerReturnValue</i> parameter should be checked for the server error code.




## -remarks



The <b>ldap_start_tls_s</b> function is called on an existing LDAP session to initiate the use of  TLS (SSL) encryption. The connection must not already have TLS (SSL) encryption enabled, and neither signing nor sealing can already be enabled. Also, a bind cannot be currently in progress on the connection, nor can there be any outstanding LDAP requests on the connection. If these conditions are not met, <b>LDAP_UNWILLING_TO_PERFORM</b> is returned. If these conditions are met, the function will send the appropriate extended operation to the server to initiate TLS (SSL), and then negotiate the encryption with the server. If the server rejects the extended operation, <b>LDAP_OTHER</b> will be returned, and the <i>ServerReturnValue</i> should be checked to retrieve the server error code.

It is possible that the server will return a referral in response to this call. For security reasons, the referral will not be automatically chased. A pointer to the referral message is returned in the <i>result</i> parameter.

After <b>ldap_start_tls_s</b> is called, automatic referral chasing and autoreconnect are disabled on the connection. They will be restored to their previous settings upon successful completion of the <a href="https://msdn.microsoft.com/7b82e79f-009e-4224-b4ce-12b60e0c1011">ldap_stop_tls_s</a> operation.

This function has a default timeout of about thirty seconds. That timeout is used in waiting for responses from the server for the Start TLS extended operation and during the TLS (SSL) negotiation.

For more information about start-stop TLS encryption, see <a href="https://msdn.microsoft.com/10e97876-21ae-49d3-9cf7-890e95b0e93d">Using Start-Stop TLS Encryption</a>.




## -see-also




<a href="https://msdn.microsoft.com/10e97876-21ae-49d3-9cf7-890e95b0e93d">Using Start-Stop TLS Encryption</a>



<a href="https://msdn.microsoft.com/7b82e79f-009e-4224-b4ce-12b60e0c1011">ldap_stop_tls_s</a>
 

 

