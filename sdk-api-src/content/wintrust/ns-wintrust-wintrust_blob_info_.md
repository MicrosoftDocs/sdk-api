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

# WINTRUST_BLOB_INFO_ structure


## -description


<p class="CCE_Message">[The  <b>WINTRUST_BLOB_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_BLOB_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a memory <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.<div class="alert"><b>Note</b>  This structure is not currently supported for the following Inbox file formats. There may be other formats besides these that are not supported. <ul>
<li>Portable executable (such as .exe, .dll, .ocx)</li>
<li>Cab files (.cab)</li>
<li>Catalog files (.cat)</li>
</ul>
This structure is only supported by files formats with <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) providers that support this structure.</div>
<div> </div>



## -struct-fields




### -field cbStruct

The number of bytes in this structure.


### -field gSubject

The <b>GUID</b> of the SIP to load.


### -field pcwszDisplayName

A string that contains the name of the memory object pointed to by <b>pbMem</b>.


### -field cbMemObject

The length, in bytes, of the memory BLOB to be verified.


### -field pbMemObject

A pointer to a memory BLOB to be verified.


### -field cbMemSignedMsg

This member is reserved. Do not use it.


### -field pbMemSignedMsg

This member is reserved. Do not use it.

