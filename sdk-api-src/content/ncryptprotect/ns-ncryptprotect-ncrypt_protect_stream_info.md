---
UID: NS:ncryptprotect.NCRYPT_PROTECT_STREAM_INFO
title: NCRYPT_PROTECT_STREAM_INFO (ncryptprotect.h)
author: windows-sdk-content
description: Is used by the NCryptStreamOpenToProtect and NCryptStreamOpenToUnprotect functions to pass blocks of processed data to your application.
old-location: security\ncrypt_protect_stream_info.htm
tech.root: SecCNG
ms.assetid: 77FADFC1-6C66-4801-B0BD-263963555C3C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NCRYPT_PROTECT_STREAM_INFO, NCRYPT_PROTECT_STREAM_INFO structure [Security], PNCRYPT_PROTECT_STREAM_INFO, PNCRYPT_PROTECT_STREAM_INFO structure pointer [Security], ncryptprotect/NCRYPT_PROTECT_STREAM_INFO, ncryptprotect/PNCRYPT_PROTECT_STREAM_INFO, security.ncrypt_protect_stream_info
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
ms.custom: 19H1
---

# NCRYPT_PROTECT_STREAM_INFO structure


## -description


The <b>NCRYPT_PROTECT_STREAM_INFO</b> structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> functions to pass blocks of processed data to your application.


## -struct-fields




### -field pfnStreamOutput

Address of a callback function that accepts data from the stream encryption or decryption process. for more information, see <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nc-ncryptprotect-pfncryptstreamoutputcallback">PFNCryptStreamOutputCallback</a>.


### -field pvCallbackCtxt

Pointer to a buffer supplied the caller. The buffer is not modified by the data protection API. You can use the buffer to keep track of your application.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nc-ncryptprotect-pfncryptstreamoutputcallback">PFNCryptStreamOutputCallback</a>
 

 

