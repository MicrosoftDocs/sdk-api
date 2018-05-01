---
UID: NS:sspi._SecPkgContext_StreamSizes
title: "_SecPkgContext_StreamSizes"
author: windows-driver-content
description: Indicates the sizes of the various parts of a stream for use with the message support functions. The QueryContextAttributes (General) function uses this structure.
old-location: security\secpkgcontext_streamsizes.htm
old-project: SecAuthN
ms.assetid: 75e5fc96-56cc-4713-a34f-fca687798ad6
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PSecPkgContext_StreamSizes, PSecPkgContext_StreamSizes, PSecPkgContext_StreamSizes structure pointer [Security], SecPkgContext_DatagramSizes, SecPkgContext_StreamSizes, SecPkgContext_StreamSizes structure [Security], _SecPkgContext_StreamSizes, _ssp_secpkgcontext_streamsizes, security.secpkgcontext_streamsizes, sspi/PSecPkgContext_StreamSizes, sspi/SecPkgContext_StreamSizes"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SecPkgContext_StreamSizes, *PSecPkgContext_StreamSizes
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgContext_StreamSizes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _SecPkgContext_StreamSizes structure


## -description



			The <b>SecPkgContext_StreamSizes</b> structure indicates the sizes of the various parts of a stream for use with the message support functions. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.


## -struct-fields




### -field cbHeader

Specifies the size, in bytes, of the header portion. If zero, no header is used.


### -field cbTrailer

Specifies the maximum size, in bytes, of the trailer portion. If zero, no trailer is used.


### -field cbMaximumMessage

Specifies the size, in bytes, of the largest message that can be encapsulated.


### -field cBuffers

Specifies the number of buffers to pass.


### -field cbBlockSize

Specifies the preferred integral size of the messages. For example, eight indicates that messages should be of size zero mod eight for optimal performance. Messages other than this block size can be padded.


## -remarks



Applications calling <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage (General)</a> should check the values of the <b>cbHeader</b>, <b>cbTrailer</b>, and <b>cbMaximumMessage</b> members to determine the size of the encrypted packet.




## -see-also




<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>
 

 

