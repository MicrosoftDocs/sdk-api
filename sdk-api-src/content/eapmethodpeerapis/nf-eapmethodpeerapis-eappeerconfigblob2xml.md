---
UID: NF:eapmethodpeerapis.EapPeerConfigBlob2Xml
title: EapPeerConfigBlob2Xml function (eapmethodpeerapis.h)
description: Converts the configuration BLOB to XML. (EapPeerConfigBlob2Xml)
helpviewer_keywords: ["EapPeerConfigBlob2Xml","EapPeerConfigBlob2Xml function [EAPHost]","eaphost.eappeerconfigblob2xml","eapmethodpeerapis/EapPeerConfigBlob2Xml"]
old-location: eaphost\eappeerconfigblob2xml.htm
tech.root: eaphost
ms.assetid: 0b6c8047-08bb-4cb7-9ef2-81793a497c65
ms.date: 12/05/2018
ms.keywords: EapPeerConfigBlob2Xml, EapPeerConfigBlob2Xml function [EAPHost], eaphost.eappeerconfigblob2xml, eapmethodpeerapis/EapPeerConfigBlob2Xml
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerConfigBlob2Xml
 - eapmethodpeerapis/EapPeerConfigBlob2Xml
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerConfigBlob2Xml
---

# EapPeerConfigBlob2Xml function


## -description

Converts the configuration BLOB to XML. The configuration BLOB is returned in the  <i>ppConnectionDataOut</i> parameter of the  <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeconfigui">EapPeerInvokeConfigUI</a> function.

## -parameters

### -param dwFlags [in]

Not used. Set to 0.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param pConfigIn [in]

A pointer to a buffer that  contains the configuration BLOB to convert.  The buffer is of size <i>dwSizeOfConfigIn</i>

### -param dwSizeOfConfigIn [in]

The size, in bytes, of the configuration BLOB.

### -param ppConfigDoc [out]

A pointer to a pointer to an XML document that  contains the converted configuration. If the EAP method does not support
                the [EapHostConfig Schema](/windows/win32/eaphost/eaphostconfigschema-schema) configuration element.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)
