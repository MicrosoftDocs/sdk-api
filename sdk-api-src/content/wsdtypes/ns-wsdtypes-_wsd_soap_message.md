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

# _WSD_SOAP_MESSAGE structure


## -description


The contents of a WSD SOAP message. This structure is used for <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> messages, ProbeMatch messages, <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a>  messages, and ResolveMatch messages, among others. 


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/6a0f0fd3-486e-45b3-bac6-e241bce8e2dc">WSD_SOAP_HEADER</a> structure that specifies the header of the SOAP message.


### -field Body

The body of the SOAP message.


### -field BodyType

Reference to a <a href="https://msdn.microsoft.com/dc214dfb-1717-4f84-af4d-6eb8cf17522c">WSDXML_TYPE</a> structure that specifies the type of the SOAP message body.


## -see-also




<a href="https://msdn.microsoft.com/52282990-d993-4034-a791-2ee7c9c1663d">Discovery and Metadata Exchange Messages</a>
 

 

