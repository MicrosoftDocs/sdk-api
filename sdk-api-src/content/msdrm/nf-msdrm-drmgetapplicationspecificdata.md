---
UID: NF:msdrm.DRMGetApplicationSpecificData
title: DRMGetApplicationSpecificData function (msdrm.h)
description: Retrieves a name-value pair of arbitrary application-specific information.
helpviewer_keywords: ["DRMGetApplicationSpecificData","DRMGetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetApplicationSpecificData","rm.drmgetapplicationspecificdata"]
old-location: rm\drmgetapplicationspecificdata.htm
tech.root: rm
ms.assetid: 49b23f00-bc73-4f51-8bbe-f523ae2408d7
ms.date: 12/05/2018
ms.keywords: DRMGetApplicationSpecificData, DRMGetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetApplicationSpecificData, rm.drmgetapplicationspecificdata
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
 - DRMGetApplicationSpecificData
 - msdrm/DRMGetApplicationSpecificData
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
 - DRMGetApplicationSpecificData
---

# DRMGetApplicationSpecificData function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetApplicationSpecificData</b> function retrieves a name-value pair of arbitrary application-specific information.

## -parameters

### -param hIssuanceLicense [in]

A handle to the issuance license to obtain the data from.

### -param uIndex [in]

The zero-based index of the name-value pair in the array of stored name-value pairs to retrieve.

### -param puNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.

### -param wszName [out]

A pointer to a Unicode character buffer that receives the name portion of the name-value pair. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> value.

### -param puValueLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszValue</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszValue</i> buffer.

### -param wszValue [out]

A pointer to a Unicode character buffer that receives the value portion of the name-value pair. The size of this buffer is specified by the <i>puValueLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puValueLength</i> value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function can be used to retrieve arbitrary information that was stored in the issuance license by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetapplicationspecificdata">DRMSetApplicationSpecificData</a> function.

The calling application is responsible for memory allocation/deallocation for variables used to hold retrieved data. To determine the size of the data that will be returned, call this function with <b>NULL</b> in <i>wszValue</i> and <i>wszName</i> to retrieve data sizes from <i>puNameLength</i> and <i>puValueLength</i>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetapplicationspecificdata">DRMSetApplicationSpecificData</a>