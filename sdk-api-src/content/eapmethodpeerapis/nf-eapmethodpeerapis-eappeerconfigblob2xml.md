---
UID: NF:eapmethodpeerapis.EapPeerConfigBlob2Xml
title: EapPeerConfigBlob2Xml function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Converts the configuration BLOB to XML.
old-location: eaphost\eappeerconfigblob2xml.htm
tech.root: eaphost
ms.assetid: 0b6c8047-08bb-4cb7-9ef2-81793a497c65
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerConfigBlob2Xml, EapPeerConfigBlob2Xml function [EAPHost], eaphost.eappeerconfigblob2xml, eapmethodpeerapis/EapPeerConfigBlob2Xml
ms.topic: function
f1_keywords:
- eapmethodpeerapis/EapPeerConfigBlob2Xml
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerConfigBlob2Xml function


## -description


Converts the configuration BLOB to XML. The configuration BLOB is returned in the  <i>ppConnectionDataOut</i> parameter of the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui">EapPeerInvokeConfigUI</a> function.


## -parameters




### -param dwFlags [in]

Not used. Set to 0.


### -param eapMethodType [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param pConfigIn [in]

A pointer to a buffer that  contains the configuration BLOB to convert.  The buffer is of size <i>dwSizeOfConfigIn</i>


### -param dwSizeOfConfigIn [in]

The size, in bytes, of the configuration BLOB.


### -param ppConfigDoc [out]

A pointer to a pointer to an XML document that  contains the converted configuration. If the EAP method does not support
                the <b>EapPeerConfigBlob2Xml </b>function, the XML document will contain the  <b>ConfigBlob</b> node with the BLOB in string form. The EAP method should create configuration inside the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphostconfigschema-schema">EapHostConfig Schema</a> configuration element.


### -param ppEapError [out]

A pointer to the address of an <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphost-peer-method-configuration-functions">EAPHost Peer Method Configuration Functions</a>
 

 

