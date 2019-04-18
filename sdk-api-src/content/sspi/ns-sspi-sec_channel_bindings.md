---
UID: NS:sspi._SEC_CHANNEL_BINDINGS
title: SEC_CHANNEL_BINDINGS (sspi.h)
author: windows-sdk-content
description: Specifies channel binding information for a security context.
old-location: security\sec_channel_bindings.htm
tech.root: SecAuthN
ms.assetid: 1cdbe53f-3fa0-46b1-9449-8fd3db6cddce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSEC_CHANNEL_BINDINGS, PSEC_CHANNEL_BINDINGS, PSEC_CHANNEL_BINDINGS structure pointer [Security], SEC_CHANNEL_BINDINGS, SEC_CHANNEL_BINDINGS structure [Security], security.sec_channel_bindings, sspi/PSEC_CHANNEL_BINDINGS, sspi/SEC_CHANNEL_BINDINGS"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_CHANNEL_BINDINGS
product: Windows
targetos: Windows
req.typenames: SEC_CHANNEL_BINDINGS, *PSEC_CHANNEL_BINDINGS
req.redist: 
ms.custom: 19H1
---

# SEC_CHANNEL_BINDINGS structure


## -description


Specifies channel binding information for a security <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.


## -struct-fields




### -field dwInitiatorAddrType

The type of  address (for example, HTTP) specified for the client.


### -field cbInitiatorLength

The size, in bytes, of the data that specifies the client address.


### -field dwInitiatorOffset

The number of bytes from the beginning of this structure to the beginning of the data that specifies the client address.


### -field dwAcceptorAddrType

The type of  address (for example, SPN) specified for the server.


### -field cbAcceptorLength

The size, in bytes, of the data that specifies the server address.


### -field dwAcceptorOffset

The number of bytes from the beginning of this structure to the beginning of the data that specifies the server address.


### -field cbApplicationDataLength

The size, in bytes, of the channel binding data.


### -field dwApplicationDataOffset

The size, in  bytes, of this structure. The channel binding data immediately follows this structure.


## -remarks



Schannel sets  to zero the value of all members of this structure other than <b>cbApplicationDataLength</b> and <b>dwApplicationDataOffset</b>.

<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security support providers</a> (SSPs) other than Schannel should use the values of this structure obtained by a call to the <a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a> function  to pass as a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure of type <b>SECBUFFER_CHANNEL_BINDINGS</b> as one of the buffers in the <i>pInput</i> parameter of a call to the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.

An <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) other than Schannel should obtain the channel binding information specified by this structure by calling the <a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a> function on the Schannel context that the client used to authenticate. Pass this channel binding information as a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure of type <b>SECBUFFER_CHANNEL_BINDINGS</b> to the <i>pInput</i> parameter of a call to the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.

 If the value of the <i>ulAttribute</i> parameter of the <a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a> function is <b>SECPKG_ATTR_UNIQUE_BINDINGS</b>, the channel binding data specified by this structure begins with "tls-unique:".

If the value of the <i>ulAttribute</i> parameter of the <a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a> function is <b>SECPKG_ATTR_ENDPOINT_BINDINGS</b>, the channel binding data specified by this structure begins with "tls-server-end-point:".




## -see-also




<a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a>



<a href="https://msdn.microsoft.com/6823cc31-acd3-4d67-92c6-65ff4d1c6aed">SecPkgContext_Bindings</a>
 

 

