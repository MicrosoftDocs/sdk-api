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

# _CREDSSP_SUBMIT_TYPE enumeration


## -description


The <b>CREDSPP_SUBMIT_TYPE</b> enumeration specifies the type of credentials specified by a <a href="https://msdn.microsoft.com/b22bd22c-e6e1-4817-b5cf-ab49f574e75f">CREDSSP_CRED</a> structure.


## -enum-fields




### -field CredsspPasswordCreds

The credentials are a user name and password.


### -field CredsspSchannelCreds

The credentials are Schannel credentials.


### -field CredsspCertificateCreds

The credentials are in a certificate.


### -field CredsspSubmitBufferBoth

The credentials contain both certificate and Schannel credentials.


### -field CredsspSubmitBufferBothOld


### -field CredsspCredEx




## -see-also




<a href="https://msdn.microsoft.com/b22bd22c-e6e1-4817-b5cf-ab49f574e75f">CREDSSP_CRED</a>
 

 

