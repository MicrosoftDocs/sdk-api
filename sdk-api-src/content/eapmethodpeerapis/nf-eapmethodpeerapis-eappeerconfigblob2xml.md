---
UID: NF:eapmethodpeerapis.EapPeerConfigBlob2Xml
title: EapPeerConfigBlob2Xml function
author: windows-sdk-content
description: Converts the configuration BLOB to XML.
old-location: eaphost\eappeerconfigblob2xml.htm
tech.root: EAPHost
ms.assetid: 0b6c8047-08bb-4cb7-9ef2-81793a497c65
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapPeerConfigBlob2Xml, EapPeerConfigBlob2Xml function [EAPHost], eaphost.eappeerconfigblob2xml, eapmethodpeerapis/EapPeerConfigBlob2Xml
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
 - EapPeerConfigBlob2Xml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerConfigBlob2Xml function


## -description


Converts the configuration BLOB to XML. The configuration BLOB is returned in the  <i>ppConnectionDataOut</i> parameter of the  <a href="https://msdn.microsoft.com/ac15a065-d0a3-403f-ae5f-175f77e2507f">EapPeerInvokeConfigUI</a> function.


## -parameters




### -param dwFlags [in]

Not used. Set to 0.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param pConfigIn [in]

A pointer to a buffer that  contains the configuration BLOB to convert.  The buffer is of size <i>dwSizeOfConfigIn</i>


### -param dwSizeOfConfigIn [in]

The size, in bytes, of the configuration BLOB.


### -param ppConfigDoc [out]

A pointer to a pointer to an XML document that  contains the converted configuration. If the EAP method does not support
                the <b>EapPeerConfigBlob2Xml </b>function, the XML document will contain the  <b>ConfigBlob</b> node with the BLOB in string form. The EAP method should create configuration inside the  <a href="https://msdn.microsoft.com/e1e4dda3-6bf4-4da5-9e14-63548ec86836">EapHostConfig Schema</a> configuration element.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/ba5c90b2-5185-4810-84a2-d08e62e8105c">EAPHost Peer Method Configuration Functions</a>
 

 

