---
UID: NF:msdrm.DRMEncode
title: DRMEncode function (msdrm.h)
description: Encodes data using a public encoding method, such as base64.
helpviewer_keywords: ["DRMEncode","DRMEncode function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMEncode","rm.drmencode"]
old-location: rm\drmencode.htm
tech.root: rm
ms.assetid: 5fc0275c-098b-43a6-a52a-871321b0e4f3
ms.date: 12/05/2018
ms.keywords: DRMEncode, DRMEncode function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMEncode, rm.drmencode
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
 - DRMEncode
 - msdrm/DRMEncode
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
 - DRMEncode
---

# DRMEncode function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMEncode</b> function encodes data using a public encoding method, such as base64.

## -parameters

### -param wszAlgID [in]

The encoding algorithm. Currently the only valid value is "base64".

### -param uDataLen [in]

Length of the input data, in bytes.

### -param pbDecodedData [in]

Pointer to the data to encode.

### -param puEncodedStringLen [in, out]

Length of the output data, in bytes.

### -param wszEncodedString [out]

The encoded string.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Note that encoding is not encrypting. Encoding does not protect content, but transforms it into a format appropriate for a specific use.

Buffer space for the encoded data must be allocated and freed by the caller. The size necessary for this buffer can be determined by calling this function with <b>NULL</b> in the <i>wszEncodedString</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdecode">DRMDecode</a>