---
UID: NF:winldap.ldap_sasl_bindW
title: ldap_sasl_bindW function (winldap.h)
author: windows-sdk-content
description: The ldap_sasl_bind is an asynchronous function that authenticates a client to the LDAP server using SASL.
old-location: ldap\ldap_sasl_bind.htm
tech.root: ldap
ms.assetid: 0de57c82-3d8e-4faa-b1ca-4559ecc326b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_sasl_bind, ldap.ldap__sasl__bind, ldap.ldap_sasl_bind, ldap_sasl_bind, ldap_sasl_bind function [LDAP], ldap_sasl_bindA, ldap_sasl_bindW, winldap/ldap_sasl_bind, winldap/ldap_sasl_bindA, winldap/ldap_sasl_bindW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_sasl_bindW (Unicode) and ldap_sasl_bindA (ANSI)
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
 - ldap_sasl_bind
 - ldap_sasl_bindA
 - ldap_sasl_bindW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_sasl_bindW function


## -description


The <b>ldap_sasl_bind</b> is an asynchronous function that authenticates a client to the LDAP server using SASL.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param DistName [in]

The distinguished name of the entry used to bind.


### -param AuthMechanism [in]

Indicates the authentication method to use.


### -param cred [in]

The credentials to use for authentication. Arbitrary credentials can be passed using this parameter. The format and content of the credentials depend on the value of the <i>AuthMechanism</i> argument passed. For more information, see Remarks.


### -param ServerCtrls [in]

A list of LDAP server controls.


### -param ClientCtrls [in]

A list of LDAP client controls.


### -param MessageNumber [out]

The message ID for the bind operation.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_sasl_bind</b> routine binds to an LDAP server using the Simple Authentication and Security Layer (SASL) protocol. The bind operation identifies a client to the directory server by providing a distinguished name and some type of authentication credentials. The authentication method being used determines the particular type of credential, and is specified by the <i>AuthMechanism</i> argument. This is passed as a string in the form of "<b>GSSAPI</b>", "<b>GSS-SPNEGO</b>", "<b>DIGEST-MD5</b>", and so on. This function can be used to pass arbitrary credentials to the server, so the application must be ready to interpret the response sent back from the server.

<div class="alert"><b>Note</b>  The Microsoft LDAP client uses a default timeout value of 120 seconds (2 minutes) for each bind-response roundtrip. This timeout value can be changed using the <b>LDAP_OPT_TIMELIMIT</b> session option. Other operations do not have a timeout unless specified using 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a>



<a href="https://msdn.microsoft.com/8347e2f5-bc14-480f-ba96-044ef3280418">ldap_sasl_bind_s</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>



<a href="https://msdn.microsoft.com/c3edca12-2dde-4f64-a479-2fbda8a4a996">ldap_simple_bind_s</a>
 

 

