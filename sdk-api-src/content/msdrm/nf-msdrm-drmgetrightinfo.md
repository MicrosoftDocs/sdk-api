---
UID: NF:msdrm.DRMGetRightInfo
title: DRMGetRightInfo function (msdrm.h)
description: Obtains information about a previously created right.
helpviewer_keywords: ["DRMGetRightInfo","DRMGetRightInfo function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetRightInfo","rm.drmgetrightinfo"]
old-location: rm\drmgetrightinfo.htm
tech.root: rm
ms.assetid: 54581da2-d3d1-44ee-936a-568b7d66143b
ms.date: 12/05/2018
ms.keywords: DRMGetRightInfo, DRMGetRightInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetRightInfo, rm.drmgetrightinfo
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
 - DRMGetRightInfo
 - msdrm/DRMGetRightInfo
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
 - DRMGetRightInfo
---

# DRMGetRightInfo function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetRightInfo</b> function obtains information about a previously created right.

## -parameters

### -param hRight [in]

The handle of the right to retrieve information from.

### -param puRightNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszRightName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszRightName</i> buffer.

### -param wszRightName [out]

A pointer to a null-terminated Unicode string that receives the name of the right. The size of this buffer is specified by the <i>puRightNameLength</i> parameter. If this information is not required, set this parameter to <b>NULL</b>.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puRightNameLength</i> value.

### -param pstFrom [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the starting validity time, in UTC time, of the right. If this information is not required, set this parameter to <b>NULL</b>.

### -param pstUntil [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the ending validity time, in UTC time, of the right. If this information is not required, set this parameter to <b>NULL</b>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a>