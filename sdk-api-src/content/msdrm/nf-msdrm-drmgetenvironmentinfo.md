---
UID: NF:msdrm.DRMGetEnvironmentInfo
title: DRMGetEnvironmentInfo function (msdrm.h)
description: Returns information about a secure environment.
helpviewer_keywords: ["DRMGetEnvironmentInfo","DRMGetEnvironmentInfo function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetEnvironmentInfo","rm.drmgetenvironmentinfo"]
old-location: rm\drmgetenvironmentinfo.htm
tech.root: rm
ms.assetid: 6b6dd54f-1835-42da-b151-9da9139efeb3
ms.date: 12/05/2018
ms.keywords: DRMGetEnvironmentInfo, DRMGetEnvironmentInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetEnvironmentInfo, rm.drmgetenvironmentinfo
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
req.product: Rights Management Services client 1.0 or later
ms.custom: 19H1
f1_keywords:
 - DRMGetEnvironmentInfo
 - msdrm/DRMGetEnvironmentInfo
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
 - DRMGetEnvironmentInfo
---

# DRMGetEnvironmentInfo function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMGetEnvironmentInfo</b> function is no longer supported and returns S_OK. Instead, use the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetinfo">DRMGetInfo</a> function.]

The <b>DRMGetEnvironmentInfo</b> function returns information about a secure environment.

## -parameters

### -param handle [in]

Environment handle.

### -param wszAttribute [in]

The attribute to query for. In Rights Management Services client 1.0 SP1, the only supported attribute is <b>g_wszQUERY_BLOCKSIZE</b>. In Rights Management Services client 1.0, the attributes that can be queried are listed in the header file Msdrmgetinfo.h. Attributes include <b>g_wszQUERY_MANIFESTSOURCE</b> and <b>g_wszQUERY_APIVERSION</b>.

### -param peEncoding [out]

Encoding type used.

### -param pcBuffer [in, out]

A pointer to a UINT value that, on input, contains the size of the buffer pointed to by the <i>pbBuffer</i> parameter. The size of the buffer is expressed as the number of Unicode characters, including the terminating null character. On output, the value contains the number of characters copied to the buffer. The number copied includes the terminating null character.

### -param pbBuffer [out]

A pointer to a null-terminated Unicode string that receives the value associated with the attribute specified by the <i>wszAttribute</i> parameter. The size of this buffer is specified by the <i>pcBuffer</i> parameter. The size is expressed as the number of Unicode characters, including the terminating null character.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function returns information only about environment handles. For information about other handles, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetinfo">DRMGetInfo</a>.

Memory allocation and deallocation are handled by the caller.To create a buffer and retrieve environment information, perform the following steps:

<ol>
<li>Call <b>DRMGetEnvironmentInfo</b> with <i>pbBuffer</i> equal to <b>NULL</b>. The function returns the required number of Unicode characters, including the terminating NULL character, in the <i>pcBuffer</i> parameter.</li>
<li>Allocate memory for the buffer. Remember that a Unicode character is two bytes long.</li>
<li>Call <b>DRMGetEnvironmentInfo</b> again with 
<i>pbBuffer</i> equal to the pointer you created when allocating the buffer.</li>
<li>When you have finished using the memory, free it.</li>
</ol>


In Rights Management Services client 1.0 SP1, the only supported attribute is <b>g_wszQUERY_BLOCKSIZE</b>. For the attributes that can be queried in Rights Management Services client 1.0, see the Msdrmgetinfo.h header file that installs with this SDK.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetinfo">DRMGetInfo</a>