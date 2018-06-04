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

# _XHR_CERT_ERROR_FLAG enumeration


## -description


Defines flags that indicate server certificate errors during SSL negotiation with the server by handling the <a href="https://msdn.microsoft.com/5b00ab76-880b-4450-a6b2-fda399cc9e8b">OnServerCertificateReceived</a> method on the <a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a> interface.


## -enum-fields




### -field XHR_CERT_ERROR_REVOCATION_FAILED

The certificate received from the server has an invalid certificate revocation.


### -field XHR_CERT_ERROR_UNKNOWN_CA

The certificate received from the server has an unknown or invalid certificate authority.


### -field XHR_CERT_ERROR_CERT_CN_INVALID

The certificate received from the server has an invalid common name.


### -field XHR_CERT_ERROR_CERT_DATE_INVALID

The certificate received from the server has an invalid certificate date. 


### -field XHR_CERT_ERROR_ALL_SERVER_ERRORS

The certificate received from the server has an invalid certificate revocation, and unknown or invalid certificate authority, an invalid common name, and an invalid certificate date.


## -see-also




<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/5b00ab76-880b-4450-a6b2-fda399cc9e8b">OnServerCertificateReceived</a>
 

 

