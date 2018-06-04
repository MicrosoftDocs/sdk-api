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

# DRMGetInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetInfo</b> function retrieves information about encrypting or decrypting objects.


## -parameters




### -param handle [in]

Specifies the handle to query. This can be created by using one of the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/133582e2-6396-476f-a28b-37ed0257fb79">DRMCreateEnablingBitsDecryptor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f3875ddd-293e-4abb-b468-a6754bc361a0">DRMCreateEnablingBitsEncryptor</a>
</li>
</ul>
<div class="alert"><b>Note</b>  You can specify only the handle of an encrypting or a decrypting object. If you specify any other handle, the function returns <b>E_DRM_INVALID_HANDLE</b>.</div>
<div> </div>

### -param wszAttribute [in]

The attribute of the handle to query for. The supported attributes are <b>g_wszQUERY_BLOCKSIZE</b>, to determine the block size, and <b>g_wszQUERY_SYMMETRICKEY_TYPE</b>, to determine whether the cipher mode is AES ECB or AES CBC 4K. 

<div class="alert"><b>Note</b>  You can use <b>g_wszQUERY_SYMMETRICKEY_TYPE</b> only in Windows 7. It is not available for earlier versions of AD RMS.</div>
<div> </div>

### -param peEncoding [out]

Pointer to a <a href="https://msdn.microsoft.com/7859d7e9-aec4-4255-a11b-5d18c08fd6ca">DRMENCODINGTYPE</a> enumeration that identifies the type of encoding to be applied to the information retrieved.


### -param pcBuffer [in, out]

A pointer to a <b>UINT</b> value that, on input, contains the size of the buffer pointed to by the <i>pbBuffer</i> parameter. The size of the buffer is expressed as the number of Unicode characters, including the terminating null character. On output, the value contains the number of characters copied to the buffer. The number copied includes the terminating null character.


### -param pbBuffer [out]

A pointer to a null-terminated Unicode string that receives the value associated with the attribute specified by the <i>wszAttribute</i> parameter. The size of this buffer is specified by the <i>pcBuffer</i> parameter. The size is expressed as the number of Unicode characters, including the terminating null character.

<div class="alert"><b>Important</b>  If the publishing license was signed using the <b>AES_CBC4K</b> value, and the <i>wszAttribute</i> parameter is specified as <b>g_wszQUERY_BLOCKSIZE</b>, <i>pbBuffer</i> returns a value of <b>4096</b>.</div>
<div> </div>
<div class="alert"><b>Important</b>  If <i>wszAttribute</i> is specified as <b>g_wszQUERY_SYMMETRICKEY_TYPE</b>, possible values for <i>pbBuffer</i> include <b>AES</b> for ECB encryption and <b>AES_CBC4K</b> for CBC encryption.</div>
<div> </div>

## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Memory allocation and deallocation are handled by the caller. To create a buffer and retrieve information, call this function twice.<ol>
<li>Set <i>pbBuffer</i> to <b>NULL</b> and call <b>DRMGetInfo</b>. The function returns the required number of Unicode characters, including the terminating <b>NULL</b> character, in the <i>pcBuffer</i> parameter.</li>
<li>Allocate memory for the buffer. Remember that a Unicode character is two bytes long.</li>
<li>Call <b>DRMGetInfo</b> again with 
<i>pbBuffer</i> equal to the pointer you created when allocating the buffer.</li>
<li>Free the allocated memory when you are finished using it.</li>
</ol>


To retrieve  information about the secure environment, you can call the <a href="https://msdn.microsoft.com/6b6dd54f-1835-42da-b151-9da9139efeb3">DRMGetEnvironmentInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/6b6dd54f-1835-42da-b151-9da9139efeb3">DRMGetEnvironmentInfo</a>
 

 

