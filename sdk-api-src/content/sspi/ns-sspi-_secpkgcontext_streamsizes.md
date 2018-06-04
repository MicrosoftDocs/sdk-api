---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

