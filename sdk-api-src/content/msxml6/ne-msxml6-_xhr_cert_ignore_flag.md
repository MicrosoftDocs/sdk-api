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

# _XHR_CERT_IGNORE_FLAG enumeration


## -description


Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the <a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a> method on the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>  interface.


## -enum-fields




### -field XHR_CERT_IGNORE_REVOCATION_FAILED

Ignore certificate revocation errors.


### -field XHR_CERT_IGNORE_UNKNOWN_CA

Ignore a certificate error for an unknown or invalid certificate authority.


### -field XHR_CERT_IGNORE_CERT_CN_INVALID

Ignore a certificate error caused by an invalid common name. This allows an invalid common name in a certificate where the server name specified by the app for the requested URL does not match the common name in the server certificate.


### -field XHR_CERT_IGNORE_CERT_DATE_INVALID

Ignore a certificate error caused by an invalid date in the certificate. This allows certificates that are expired or not yet effective.


### -field XHR_CERT_IGNORE_ALL_SERVER_ERRORS

Ignore all server certificate errors.


## -see-also




<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

