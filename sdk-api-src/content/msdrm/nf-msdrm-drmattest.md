---
UID: NF:msdrm.DRMAttest
title: DRMAttest function (msdrm.h)
description: The DRMAttest function is no longer supported and returns E_NOTIMPL.
helpviewer_keywords: ["DRMAttest","DRMAttest function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMAttest","rm.drmattest"]
old-location: rm\drmattest.htm
tech.root: rm
ms.assetid: f0975845-d609-4f7a-a663-6481334c983d
ms.date: 12/05/2018
ms.keywords: DRMAttest, DRMAttest function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAttest, rm.drmattest
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
 - DRMAttest
 - msdrm/DRMAttest
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
 - DRMAttest
---

# DRMAttest function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMAttest</b> function is no longer supported and returns E_NOTIMPL.]

For Rights Management Services 1.0, the <b>DRMAttest</b> function signs arbitrary data.

## -parameters

### -param hEnablingPrincipal [in]

A handle to an enabling principal object created by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a>.

### -param wszData [in]

The data to encode.

### -param eType [in]

An enumeration that determines whether to include full environment data or only a hash.

### -param pcAttestedBlob [in, out]

Length, in characters, of the string being returned, plus one for a terminating null character.

### -param wszAttestedBlob [out]

The signed data.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function can be used with challenge/response protocols by including the challenge in the data buffer. An output string may contain the principal's certificates, in addition to the signature.

The data is concatenated with the manifest used to initialize the RM environment. A manifest is a signed XrML blob that includes information to authenticate the program and all required DLLs, as well as a list of any prohibited DLLs. The manifest used is the one loaded when the RM environment was initialized. For information about making a manifest, see <a href="/previous-versions/windows/desktop/adrms_sdk/creating-an-application-manifest">Creating an Application Manifest</a>.

To return a value, first call this function with <b>NULL</b> passed into the <i>wszAttestedBlob</i> parameter. The value returned in <i>pcStrLen</i> will indicate the size of the variable the application must create to hold the encoded signature. All buffer allocation and destruction are the responsibility of the caller.

Data signed by using <b>DRMAttest</b> can be verified by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmverify">DRMVerify</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>