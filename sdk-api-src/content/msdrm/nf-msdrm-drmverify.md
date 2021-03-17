---
UID: NF:msdrm.DRMVerify
title: DRMVerify function (msdrm.h)
description: No longer supported and returns E_NOTIMPL.
helpviewer_keywords: ["DRMVerify","DRMVerify function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMVerify","rm.drmverify"]
old-location: rm\drmverify.htm
tech.root: rm
ms.assetid: aebf46e7-9de2-40e7-a748-0621a61ccb6a
ms.date: 12/05/2018
ms.keywords: DRMVerify, DRMVerify function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMVerify, rm.drmverify
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
 - DRMVerify
 - msdrm/DRMVerify
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
 - DRMVerify
---

# DRMVerify function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMVerify</b> function is no longer supported and returns E_NOTIMPL.]

For Rights Management Services 1.0, the <b>DRMVerify</b> function verifies data signed with <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmattest">DRMAttest</a>.

## -parameters

### -param wszData [in]

The data to verify (original data).

### -param pcAttestedData [in, out]

Length, in characters, of the data to verify, plus one for a terminating null character.

### -param wszAttestedData [out]

The signed data.

### -param peType [out]

Whether full environment information,  or just a hash of the environment, is included.

### -param pcPrincipal [in, out]

Size, in characters, of the <i>wszPrincipalCredentials</i> parameter, plus one for a terminating null character.

### -param wszPrincipal [out]

Certificate chain of the principal attesting the data. This chain is needed to create the principal used to verify the data.

### -param pcManifest [in, out]

Size, in characters, of the manifest used to sign the data, plus one for a terminating null character. For information about making a manifest, see <a href="/previous-versions/windows/desktop/adrms_sdk/creating-an-application-manifest">Creating an Application Manifest</a>.

### -param wszManifest [out]

The manifest used to sign, as a null-terminated string.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>