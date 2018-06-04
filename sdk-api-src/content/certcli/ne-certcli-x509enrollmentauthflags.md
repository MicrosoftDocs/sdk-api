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

# X509EnrollmentAuthFlags enumeration


## -description


The <b>X509EnrollmentAuthFlags</b> enumeration specifies the authentication type.


## -enum-fields




### -field X509AuthNone

Reserved.


### -field X509AuthAnonymous

Anonymous authentication.


### -field X509AuthKerberos

Kerberos authentication.


### -field X509AuthUsername

Plaintext user name and password authentication.


### -field X509AuthCertificate

A client authentication certificate (suitable for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure Sockets Layer protocol</a> (SSL) client authentication) that is installed locally and that has an associated private key.  This certificate is used by the server to verify the client's identity.

