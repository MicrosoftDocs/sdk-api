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

# EapHostPeerConfigXml2Blob function


## -description


 Converts XML into the configuration  BLOB.  When the supplicant starts authentication or calls <a href="https://msdn.microsoft.com/afb20482-a439-437d-9c8f-c4e87e440113">EapHostPeerInvokeConfigUI</a>, the supplicant calls <b>EapHostPeerConfigXml2Blob</b> to convert the XML configuration into a BLOB. 

The XML data to be converted could originate  from a <b>EapHostPeerConfigBlob2Xml</b> call, or the data could originate from a XML created by a system administrator or other XML author. 


## -parameters




### -param dwFlags [in]

Not used. Set to 0.


### -param pConfigDoc [in]

Sends a pointer to the XML configuration to be converted.


### -param pdwSizeOfConfigOut [out]

A pointer to the size, in bytes, of the configuration BLOB.


### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains the configuration data converted from XML. The configuration data is created inside <a href="https://msdn.microsoft.com/e1e4dda3-6bf4-4da5-9e14-63548ec86836">EapHostConfig Schema</a> element. The buffer is of size <i>pdwSizeOfConfigOut</i>. After consuming the data, this memory must be freed by calling <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>.  


### -param pEapMethodType [out]

A pointer to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure referred to in the XML document. 


### -param ppEapError [out]

A pointer a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised  by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/728fab9e-6aa4-49c0-ab1f-89686543524c">EapHostPeerConfigXml2Blob</a>



<a href="https://msdn.microsoft.com/e1f0fc05-d9cd-4a37-ba74-89ac9948a292">EapHostPeerGetResult</a>



<a href="https://msdn.microsoft.com/afb20482-a439-437d-9c8f-c4e87e440113">EapHostPeerInvokeConfigUI</a>
 

 

