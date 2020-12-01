---
UID: NS:sspi._CREDUIWIN_MARSHALED_CONTEXT
title: CREDUIWIN_MARSHALED_CONTEXT (sspi.h)
description: Specifies credential information that has been serialized by using the ICredentialProvider::SetSerialization method.
helpviewer_keywords: ["*PCREDUIWIN_MARSHALED_CONTEXT","CREDUIWIN_MARSHALED_CONTEXT","CREDUIWIN_MARSHALED_CONTEXT structure [Security]","PCREDUIWIN_MARSHALED_CONTEXT","PCREDUIWIN_MARSHALED_CONTEXT structure pointer [Security]","security.creduiwin_marshaled_context","sspi/CREDUIWIN_MARSHALED_CONTEXT","sspi/PCREDUIWIN_MARSHALED_CONTEXT"]
old-location: security\creduiwin_marshaled_context.htm
tech.root: security
ms.assetid: 61e0c9c8-f484-42a9-95c2-5ab77fb20c6c
ms.date: 12/05/2018
ms.keywords: '*PCREDUIWIN_MARSHALED_CONTEXT, CREDUIWIN_MARSHALED_CONTEXT, CREDUIWIN_MARSHALED_CONTEXT structure [Security], PCREDUIWIN_MARSHALED_CONTEXT, PCREDUIWIN_MARSHALED_CONTEXT structure pointer [Security], security.creduiwin_marshaled_context, sspi/CREDUIWIN_MARSHALED_CONTEXT, sspi/PCREDUIWIN_MARSHALED_CONTEXT'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: CREDUIWIN_MARSHALED_CONTEXT, *PCREDUIWIN_MARSHALED_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDUIWIN_MARSHALED_CONTEXT
 - sspi/_CREDUIWIN_MARSHALED_CONTEXT
 - PCREDUIWIN_MARSHALED_CONTEXT
 - sspi/PCREDUIWIN_MARSHALED_CONTEXT
 - CREDUIWIN_MARSHALED_CONTEXT
 - sspi/CREDUIWIN_MARSHALED_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - CREDUIWIN_MARSHALED_CONTEXT
---

# CREDUIWIN_MARSHALED_CONTEXT structure


## -description

Specifies credential information that has been serialized by using the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">ICredentialProvider::SetSerialization</a> method.

## -struct-fields

### -field StructureType

The type of the structure. This must be <b>CREDUIWIN_STRUCTURE_TYPE_SSPIPFC</b>.

### -field cbHeaderLength

The size, in bytes, of the header.

### -field LogonId

The user's logon ID.

### -field MarshaledDataType

A value that represents the type of structure that the serialized data specifies. If the value of this parameter is <b>SSPIPFC_STRUCTURE_TYPE_CREDUI_CONTEXT</b>, the data can be deserialized by calling the <a href="/windows/desktop/api/sspi/nf-sspi-sspiunmarshalcreduicontext">SspiUnmarshalCredUIContext</a> function.

### -field MarshaledDataOffset

The number of bytes from the beginning of this structure to the beginning of the serialized data.

### -field MarshaledDataLength

The size, in bytes, of the serialized data.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_credui_context">SEC_WINNT_CREDUI_CONTEXT</a>