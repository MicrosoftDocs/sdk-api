---
UID: NF:msdrm.DRMDecode
title: DRMDecode function (msdrm.h)
description: Decodes a string encoded with a common algorithm, such as base64.
helpviewer_keywords: ["DRMDecode","DRMDecode function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDecode","rm.drmdecode"]
old-location: rm\drmdecode.htm
tech.root: rm
ms.assetid: 380f9770-1d0c-453a-b737-04740608d7a7
ms.date: 12/05/2018
ms.keywords: DRMDecode, DRMDecode function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDecode, rm.drmdecode
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
 - DRMDecode
 - msdrm/DRMDecode
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
 - DRMDecode
---

# DRMDecode function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDecode</b> function decodes a string encoded with a common algorithm, such as base64.

## -parameters

### -param wszAlgID [in]

The encoding algorithm name. Currently "base64" is the only valid value.

### -param wszEncodedString [in]

The encoded string.

### -param puDecodedDataLen [in]

The length of the decoded string, in characters, plus one for a null terminator.

### -param pbDecodedData [out]

Pointer to the decoded data.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Encoding is not the same as encrypting.

Buffer space for the decoded data must be allocated and freed by the caller. The size necessary for this buffer can be determined by calling this function with <b>NULL</b> in the <i>pbDecodedData</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmencode">DRMEncode</a>