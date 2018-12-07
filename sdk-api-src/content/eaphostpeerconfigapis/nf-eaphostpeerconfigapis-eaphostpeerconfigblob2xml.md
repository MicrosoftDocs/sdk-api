---
UID: NF:eaphostpeerconfigapis.EapHostPeerConfigBlob2Xml
title: EapHostPeerConfigBlob2Xml function
author: windows-sdk-content
description: Converts the configuration BLOB to XML.
old-location: eaphost\eaphostpeerconfigblob2xml.htm
tech.root: eaphost
ms.assetid: 158750ec-cc26-4740-add6-2135b9aa294c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EapHostPeerConfigBlob2Xml, EapHostPeerConfigBlob2Xml function [EAPHost], eaphost.eaphostpeerconfigblob2xml, eaphostpeerconfigapis/EapHostPeerConfigBlob2Xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eaphostpeerconfigapis.h
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerConfigBlob2Xml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerConfigBlob2Xml function


## -description


Converts the configuration BLOB to XML. 

The configuration BLOB is returned when the supplicant called one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/728fab9e-6aa4-49c0-ab1f-89686543524c">EapHostPeerConfigXml2Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/afb20482-a439-437d-9c8f-c4e87e440113">EapHostPeerInvokeConfigUI</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1f0fc05-d9cd-4a37-ba74-89ac9948a292">EapHostPeerGetResult</a> - via the <a href="https://msdn.microsoft.com/376e5399-61c9-4927-ac68-8a1bb4bdc7db">EapHostPeerMethodResult</a> structure</li>
</ul>



## -parameters




### -param dwFlags [in]

Not used. Set to 0.


### -param eapMethodType [in]

Refers to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that is referred to in the XML document. 


### -param dwSizeOfConfigIn [in]

The size, in bytes, of the configuration BLOB.


### -param pConfigIn [in]

A pointer to a buffer that  contains the configuration BLOB to convert.  The buffer is of size <i>dwSizeOfConfigIn</i>. 


### -param ppConfigDoc [out]

A pointer to a pointer to an XML document that  contains the converted configuration. If the EAP method does not support
                the <b>EapHostPeerConfigBlob2Xml </b>function, the XML document will contain the  <b>ConfigBlob</b> node with the BLOB in string form. The EAP method should create configuration inside the <a href="https://msdn.microsoft.com/e1e4dda3-6bf4-4da5-9e14-63548ec86836">EapHostConfig Schema</a> element.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/e1e4dda3-6bf4-4da5-9e14-63548ec86836">EapHostPeerConfigXml2Blob</a>



<a href="https://msdn.microsoft.com/e1f0fc05-d9cd-4a37-ba74-89ac9948a292">EapHostPeerGetResult</a>



<a href="https://msdn.microsoft.com/afb20482-a439-437d-9c8f-c4e87e440113">EapHostPeerInvokeConfigUI</a>
 

 

