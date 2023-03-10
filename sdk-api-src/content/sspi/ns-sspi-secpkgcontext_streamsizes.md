---
UID: NS:sspi._SecPkgContext_StreamSizes
title: SecPkgContext_StreamSizes (sspi.h)
description: Indicates the sizes of the various parts of a stream for use with the message support functions. The QueryContextAttributes (General) function uses this structure.
helpviewer_keywords: ["*PSecPkgContext_StreamSizes","PSecPkgContext_StreamSizes","PSecPkgContext_StreamSizes structure pointer [Security]","SecPkgContext_DatagramSizes","SecPkgContext_StreamSizes","SecPkgContext_StreamSizes structure [Security]","_ssp_secpkgcontext_streamsizes","security.secpkgcontext_streamsizes","sspi/PSecPkgContext_StreamSizes","sspi/SecPkgContext_StreamSizes"]
old-location: security\secpkgcontext_streamsizes.htm
tech.root: security
ms.assetid: 75e5fc96-56cc-4713-a34f-fca687798ad6
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_StreamSizes, PSecPkgContext_StreamSizes, PSecPkgContext_StreamSizes structure pointer [Security], SecPkgContext_DatagramSizes, SecPkgContext_StreamSizes, SecPkgContext_StreamSizes structure [Security], _ssp_secpkgcontext_streamsizes, security.secpkgcontext_streamsizes, sspi/PSecPkgContext_StreamSizes, sspi/SecPkgContext_StreamSizes'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_StreamSizes, *PSecPkgContext_StreamSizes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_StreamSizes
 - sspi/_SecPkgContext_StreamSizes
 - PSecPkgContext_StreamSizes
 - sspi/PSecPkgContext_StreamSizes
 - SecPkgContext_StreamSizes
 - sspi/SecPkgContext_StreamSizes
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
 - SecPkgContext_StreamSizes
---

# SecPkgContext_StreamSizes structure


## -description

The <b>SecPkgContext_StreamSizes</b> structure indicates the sizes of the various parts of a stream for use with the message support functions. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

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

Applications calling <a href="/windows/desktop/api/sspi/nf-sspi-encryptmessage">EncryptMessage (General)</a> should check the values of the <b>cbHeader</b>, <b>cbTrailer</b>, and <b>cbMaximumMessage</b> members to determine the size of the encrypted packet.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>