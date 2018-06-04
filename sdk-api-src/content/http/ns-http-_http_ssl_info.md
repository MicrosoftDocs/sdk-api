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

# _HTTP_SSL_INFO structure


## -description


The 
<b>HTTP_SSL_INFO</b> structure contains data for a connection that uses Secure Sockets Layer (SSL), obtained through the SSL handshake.


## -struct-fields




### -field ServerCertKeySize

The size, in bytes, of the public key used to sign the server certificate.


### -field ConnectionKeySize

The size, in bytes, of the cipher key used to encrypt the current session.


### -field ServerCertIssuerSize

The size, in bytes, of the string pointed to by the <b>pServerCertIssuer</b> member not including the terminating null character.


### -field ServerCertSubjectSize

The size, in bytes, of the string pointed to by the <b>pServerCertSubject</b> member not including the terminating null character.


### -field pServerCertIssuer

A pointer to a null-terminated string of octets that specifies the name of the entity that issued the certificate.


### -field pServerCertSubject

A pointer to a null-terminated string of octets that specifies the name of the entity to which the certificate belongs.


### -field pClientCertInfo

A pointer to an 
<a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a> structure that specifies the client certificate.


### -field SslClientCertNegotiated

If non-zero, indicates that the client certificate is already present locally.


## -remarks



An 
<b>HTTP_SSL_INFO</b> structure can be pointed to by the <b>pSslInfo</b> member of an 
<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a>
 

 

