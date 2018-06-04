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

# PFNCryptStreamOutputCallback callback function


## -description


The <b>PFNCryptStreamOutputCallback</b> function receives encrypted or decrypted data from tasks started by using the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> or <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions. This callback must be defined by your application using the following syntax.


## -parameters




### -param *pvCallbackCtxt [in]

Pointer to data that you can use to keep track of your application. The data is not modified by the data protection API. 

<div class="alert"><b>Note</b>  You can set a pointer to your context data in the <b>pvCallbackCtxt</b> member of the <a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a> structure before passing a pointer to that structure in the <i>pStreamInfo</i> parameter of the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> or  <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions.</div>
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



 Set a pointer to this callback function in the <b>pfnStreamOutput</b> member of the  <a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a> structure. Set a pointer to the structure in the <i>pStreamInfo</i> parameter of the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> or  <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions.

You can use this callback to further process the encrypted or decrypted data. A common use of the function is to write the data to disk as it is received from the data protection API. The blocks of encrypted or unencrypted data are created by the <a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a> function.




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a>



<a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a>



<a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a>
 

 

