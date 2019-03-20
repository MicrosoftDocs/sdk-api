---
UID: NF:ncryptprotect.NCryptStreamOpenToUnprotect
title: NCryptStreamOpenToUnprotect function (ncryptprotect.h)
author: windows-sdk-content
description: Opens a stream object that can be used to decrypt large amounts of data to the same protection descriptor used for encryption.
old-location: security\ncryptstreamopentounprotect.htm
tech.root: seccng
ms.assetid: 9848082E-EDDA-4DA1-9896-42EAF2ADFAB4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptStreamOpenToUnprotect, NCryptStreamOpenToUnprotect function [Security], ncryptprotect/NCryptStreamOpenToUnprotect, security.ncryptstreamopentounprotect
ms.topic: function
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
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptStreamOpenToUnprotect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptStreamOpenToUnprotect function


## -description


The <b>NCryptStreamOpenToUnprotect</b> function opens a stream object that can be used to decrypt large amounts of data to the same  protection descriptor used for encryption. Call <a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a> to perform the decryption. To decrypt smaller messages such as keys and passwords, call <a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>.


## -parameters




### -param pStreamInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a> structure that contains the address of a user defined callback function to receive the decrypted data and a pointer to user-defined context data.


### -param dwFlags

A flag that specifies additional information for the key service provider. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider not display a user interface.

</td>
</tr>
</table>
 


### -param hWnd [in, optional]

Handle to the parent window of the user interface, if any, to be displayed.


### -param phStream [out]

Pointer to the handle of the decrypted stream of data.


## -returns



Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

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
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The dwFlags parameter must contain zero (0) or <b>NCRYPT_SILENT_FLAG</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>phStream</i> and <i>pStreamInfo</i> parameters cannot be <b>NULL</b>.

The callback function pointed to by the <b>pfnStreamOutput</b> member of the <a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a> structure pointed to by the <i>pStreamInfo</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to allocate a data stream.

</td>
</tr>
</table>
 




## -remarks



The <b>NCryptStreamOpenToUnprotect</b> function  creates an internal stream object that can be used to encrypt large messages. You cannot use the object directly. Instead, you must use the object handle returned by this function.

Call this function before calling the <a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a> function. If you are encrypting a large file, use <b>NCryptStreamUpdate</b> in a loop that advances through the file block by block, encrypting each block as it advances and notifying your callback when each block is finished. For more information, see <b>NCryptStreamUpdate</b>.

The <b>NCryptStreamOpenToUnprotect</b> function retrieves the unencrypted protection descriptor rule string from the stream header. The rule string is placed in the header by the <b>NCryptStreamOpenToUnprotect</b> function.




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/77FADFC1-6C66-4801-B0BD-263963555C3C">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="https://msdn.microsoft.com/770640F2-04C7-4512-8004-41F4ECDC110E">NCryptStreamClose</a>



<a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a>



<a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a>
 

 

