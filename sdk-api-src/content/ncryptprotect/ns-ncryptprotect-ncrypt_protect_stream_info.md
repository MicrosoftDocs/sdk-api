---
UID: NS:ncryptprotect.NCRYPT_PROTECT_STREAM_INFO
title: NCRYPT_PROTECT_STREAM_INFO
author: windows-sdk-content
description: Is used by the NCryptStreamOpenToProtect and NCryptStreamOpenToUnprotect functions to pass blocks of processed data to your application.
old-location: security\ncrypt_protect_stream_info.htm
tech.root: seccng
ms.assetid: 77FADFC1-6C66-4801-B0BD-263963555C3C
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: NCRYPT_PROTECT_STREAM_INFO, NCRYPT_PROTECT_STREAM_INFO structure [Security], PNCRYPT_PROTECT_STREAM_INFO, PNCRYPT_PROTECT_STREAM_INFO structure pointer [Security], ncryptprotect/NCRYPT_PROTECT_STREAM_INFO, ncryptprotect/PNCRYPT_PROTECT_STREAM_INFO, security.ncrypt_protect_stream_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - NCryptprotect.h
api_name:
 - NCRYPT_PROTECT_STREAM_INFO
product: Windows
targetos: Windows
req.typenames: NCRYPT_PROTECT_STREAM_INFO
req.redist: 
---

# NCRYPT_PROTECT_STREAM_INFO structure


## -description


The <b>NCRYPT_PROTECT_STREAM_INFO</b> structure is used by the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> and <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions to pass blocks of processed data to your application.


## -struct-fields




### -field pfnStreamOutput

Address of a callback function that accepts data from the stream encryption or decryption process. for more information, see <a href="https://msdn.microsoft.com/D07B2B63-306B-4C41-AA14-320EFEFFB939">PFNCryptStreamOutputCallback</a>.


### -field pvCallbackCtxt

Pointer to a buffer supplied the caller. The buffer is not modified by the data protection API. You can use the buffer to keep track of your application.


## -see-also




<a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a>



<a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a>



<a href="https://msdn.microsoft.com/D07B2B63-306B-4C41-AA14-320EFEFFB939">PFNCryptStreamOutputCallback</a>
 

 

