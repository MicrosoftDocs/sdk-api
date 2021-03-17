---
UID: NF:msdrm.DRMGetInfo
title: DRMGetInfo function (msdrm.h)
description: Retrieves information about encrypting or decrypting objects.
helpviewer_keywords: ["DRMGetInfo","DRMGetInfo function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetInfo","rm.drmgetinfo"]
old-location: rm\drmgetinfo.htm
tech.root: rm
ms.assetid: 6cb1275a-c0e4-48df-a389-76add74bdabd
ms.date: 12/05/2018
ms.keywords: DRMGetInfo, DRMGetInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetInfo, rm.drmgetinfo
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMGetInfo
 - msdrm/DRMGetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetInfo
---

# DRMGetInfo function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetInfo</b> function retrieves information about encrypting or decrypting objects.

## -parameters

### -param handle [in]

Specifies the handle to query. This can be created by using one of the following functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsdecryptor">DRMCreateEnablingBitsDecryptor</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsencryptor">DRMCreateEnablingBitsEncryptor</a>
</li>
</ul>
<div class="alert"><b>Note</b>  You can specify only the handle of an encrypting or a decrypting object. If you specify any other handle, the function returns <b>E_DRM_INVALID_HANDLE</b>.</div>
<div> </div>

### -param wszAttribute [in]

The attribute of the handle to query for. The supported attributes are <b>g_wszQUERY_BLOCKSIZE</b>, to determine the block size, and <b>g_wszQUERY_SYMMETRICKEY_TYPE</b>, to determine whether the cipher mode is AES ECB or AES CBC 4K. 

<div class="alert"><b>Note</b>  You can use <b>g_wszQUERY_SYMMETRICKEY_TYPE</b> only in Windows 7. It is not available for earlier versions of AD RMS.</div>
<div> </div>

### -param peEncoding [out]

Pointer to a <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drmencodingtype">DRMENCODINGTYPE</a> enumeration that identifies the type of encoding to be applied to the information retrieved.

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Memory allocation and deallocation are handled by the caller. To create a buffer and retrieve information, call this function twice.<ol>
<li>Set <i>pbBuffer</i> to <b>NULL</b> and call <b>DRMGetInfo</b>. The function returns the required number of Unicode characters, including the terminating <b>NULL</b> character, in the <i>pcBuffer</i> parameter.</li>
<li>Allocate memory for the buffer. Remember that a Unicode character is two bytes long.</li>
<li>Call <b>DRMGetInfo</b> again with 
<i>pbBuffer</i> equal to the pointer you created when allocating the buffer.</li>
<li>Free the allocated memory when you are finished using it.</li>
</ol>


To retrieve  information about the secure environment, you can call the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetenvironmentinfo">DRMGetEnvironmentInfo</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetenvironmentinfo">DRMGetEnvironmentInfo</a>