---
UID: NF:eapmethodpeerapis.EapPeerConfigXml2Blob
title: EapPeerConfigXml2Blob function
author: windows-sdk-content
description: Converts XML into the configuration BLOB.
old-location: eaphost\eappeerconfigxml2blob.htm
tech.root: EAPHost
ms.assetid: d568da63-1d12-4c02-8d84-f06fa3f8d39f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapPeerConfigXml2Blob, EapPeerConfigXml2Blob function [EAPHost], eaphost.eappeerconfigxml2blob, eapmethodpeerapis/EapPeerConfigXml2Blob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eapmethodpeerapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerConfigXml2Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerConfigXml2Blob function


## -description


 Converts XML into the configuration  BLOB.


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior. May be set to 0.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param pConfigDoc [in]

Sends a pointer to the XML configuration to be converted.


### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains the configuration data converted from XML. The configuration data is created inside the <a href="https://msdn.microsoft.com/e1e4dda3-6bf4-4da5-9e14-63548ec86836">EapHostConfig Schema</a> element. The buffer is of size <i>pdwSizeOfConfigOut</i>. After consuming the data, this memory must be freed by calling <a href="https://msdn.microsoft.com/544d999c-d857-4ca5-b5f8-b15780fc7019">EapPeerFreeMemory</a>.  


### -param pdwSizeOfConfigOut [out]

A pointer to the size, in bytes, of the configuration BLOB in <i>ppConfigBlob</i>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised  during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/ba5c90b2-5185-4810-84a2-d08e62e8105c">EAPHost Peer Method Configuration Functions</a>
 

 

