---
UID: NF:eapmethodpeerapis.EapPeerConfigXml2Blob
title: EapPeerConfigXml2Blob function (eapmethodpeerapis.h)
description: Converts XML into the configuration BLOB. (EapPeerConfigXml2Blob)
helpviewer_keywords: ["EapPeerConfigXml2Blob","EapPeerConfigXml2Blob function [EAPHost]","eaphost.eappeerconfigxml2blob","eapmethodpeerapis/EapPeerConfigXml2Blob"]
old-location: eaphost\eappeerconfigxml2blob.htm
tech.root: eaphost
ms.assetid: d568da63-1d12-4c02-8d84-f06fa3f8d39f
ms.date: 12/05/2018
ms.keywords: EapPeerConfigXml2Blob, EapPeerConfigXml2Blob function [EAPHost], eaphost.eappeerconfigxml2blob, eapmethodpeerapis/EapPeerConfigXml2Blob
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
 - EapPeerConfigXml2Blob
 - eapmethodpeerapis/EapPeerConfigXml2Blob
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
 - EapPeerConfigXml2Blob
---

# EapPeerConfigXml2Blob function


## -description

 Converts XML into the configuration  BLOB.

## -parameters

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior. May be set to 0.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param pConfigDoc [in]

Sends a pointer to the XML configuration to be converted.

### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains the configuration data converted from XML. The configuration data is created inside the [EapHostConfig Schema](/windows/win32/eaphost/eaphostconfigschema-schema) element. The buffer is of size <i>pdwSizeOfConfigOut</i>. After consuming the data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory">EapPeerFreeMemory</a>.

### -param pdwSizeOfConfigOut [out]

A pointer to the size, in bytes, of the configuration BLOB in <i>ppConfigBlob</i>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised  during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)
