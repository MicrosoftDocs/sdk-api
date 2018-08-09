---
UID: NS:sspi._CREDUIWIN_MARSHALED_CONTEXT
title: "_CREDUIWIN_MARSHALED_CONTEXT"
author: windows-sdk-content
description: Specifies credential information that has been serialized by using the ICredentialProvider::SetSerialization method.
old-location: security\creduiwin_marshaled_context.htm
old-project: secauthn
ms.assetid: 61e0c9c8-f484-42a9-95c2-5ab77fb20c6c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCREDUIWIN_MARSHALED_CONTEXT, CREDUIWIN_MARSHALED_CONTEXT, CREDUIWIN_MARSHALED_CONTEXT structure [Security], PCREDUIWIN_MARSHALED_CONTEXT, PCREDUIWIN_MARSHALED_CONTEXT structure pointer [Security], _CREDUIWIN_MARSHALED_CONTEXT, security.creduiwin_marshaled_context, sspi/CREDUIWIN_MARSHALED_CONTEXT, sspi/PCREDUIWIN_MARSHALED_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CREDUIWIN_MARSHALED_CONTEXT, *PCREDUIWIN_MARSHALED_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - CREDUIWIN_MARSHALED_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _CREDUIWIN_MARSHALED_CONTEXT structure


## -description


Specifies credential information that has been serialized by using the <a href="https://msdn.microsoft.com/en-us/library/Bb776043(v=VS.85).aspx">ICredentialProvider::SetSerialization</a> method.


## -struct-fields




### -field StructureType

The type of the structure. This must be <b>CREDUIWIN_STRUCTURE_TYPE_SSPIPFC</b>.


### -field cbHeaderLength

The size, in bytes, of the header.


### -field LogonId

The user's logon ID.


### -field MarshaledDataType

A value that represents the type of structure that the serialized data specifies. If the value of this parameter is <b>SSPIPFC_STRUCTURE_TYPE_CREDUI_CONTEXT</b>, the data can be deserialized by calling the <a href="https://msdn.microsoft.com/c8861b27-d42d-4f7f-96c7-718f23fbaf86">SspiUnmarshalCredUIContext</a> function.


### -field MarshaledDataOffset

The number of bytes from the beginning of this structure to the beginning of the serialized data.


### -field MarshaledDataLength

The size, in bytes, of the serialized data.


## -see-also




<a href="https://msdn.microsoft.com/ac9410eb-ec1b-494c-8e8b-6d161ff2b41c">SEC_WINNT_CREDUI_CONTEXT</a>
 

 

