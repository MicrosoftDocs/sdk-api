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

# _PKU2U_CERTIFICATE_S4U_LOGON structure


## -description


Specifies a certificate used for S4U logon.


## -struct-fields




### -field MessageType

A value of the <a href="https://msdn.microsoft.com/10de9dd4-0f6c-4431-a60d-9b9c60585676">PKU2U_LOGON_SUBMIT_TYPE</a> enumeration that indicates the logon type.


### -field Flags

This member is reserved. Do not use it.


### -field UserPrincipalName

The name of the user who is attempting to authenticate.


### -field DomainName

 


### -field CertificateLength

The size, in bytes, of the <b>Certificate</b> buffer.


### -field Certificate

The certificate data.


#### - UNICODE_STRING

This member is reserved. Do not use it.

