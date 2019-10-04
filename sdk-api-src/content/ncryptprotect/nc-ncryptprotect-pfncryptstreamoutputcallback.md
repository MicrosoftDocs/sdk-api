---
UID: NC:ncryptprotect.PFNCryptStreamOutputCallback
title: PFNCryptStreamOutputCallback (ncryptprotect.h)
author: windows-sdk-content
description: Receives encrypted or decrypted data from tasks started by using the NCryptStreamOpenToProtect or NCryptStreamOpenToUnprotect functions.
old-location: security\pfncryptstreamoutputcallback.htm
tech.root: SecCNG
ms.assetid: D07B2B63-306B-4C41-AA14-320EFEFFB939
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PFNCryptStreamOutputCallback, PFNCryptStreamOutputCallback callback, PFNCryptStreamOutputCallback callback function [Security], ncryptprotect/PFNCryptStreamOutputCallback, security.pfncryptstreamoutputcallback
ms.topic: callback
f1_keywords: 
 - "ncryptprotect/PFNCryptStreamOutputCallback"
dev_langs:
 - c++
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
 - UserDefined
api_location:
 - NCryptprotect.h
api_name:
 - PFNCryptStreamOutputCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFNCryptStreamOutputCallback callback function


## -description


The <b>PFNCryptStreamOutputCallback</b> function receives encrypted or decrypted data from tasks started by using the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> functions. This callback must be defined by your application using the following syntax.


## -parameters




### -param *pvCallbackCtxt [in]

Pointer to data that you can use to keep track of your application. The data is not modified by the data protection API. 

<div class="alert"><b>Note</b>  You can set a pointer to your context data in the <b>pvCallbackCtxt</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a> structure before passing a pointer to that structure in the <i>pStreamInfo</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> functions.</div>
<div> </div>

### -param *pbData [in]

Pointer to a block of processed data that can be used by the application.


### -param cbData

The size, in bytes, of the processed data pointed to by the <i>pbData</i> parameter.


### -param fFinal

If this value is <b>TRUE</b>, the current data block is the last to be processed and this
        is the last time the callback will be called.


## -returns



If you return any status code other than <b>ERROR_SUCCESS</b> from your implementation of this callback function, the stream encryption or decryption process will fail.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



 Set a pointer to this callback function in the <b>pfnStreamOutput</b> member of the  <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a> structure. Set a pointer to the structure in the <i>pStreamInfo</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> functions.

You can use this callback to further process the encrypted or decrypted data. A common use of the function is to write the data to disk as it is received from the data protection API. The blocks of encrypted or unencrypted data are created by the <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a>
 

 

