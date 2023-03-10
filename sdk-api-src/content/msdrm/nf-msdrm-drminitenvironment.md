---
UID: NF:msdrm.DRMInitEnvironment
title: DRMInitEnvironment function (msdrm.h)
description: Creates a secure environment for all rights management calls.
helpviewer_keywords: ["DRMInitEnvironment","DRMInitEnvironment function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMInitEnvironment","rm.drminitenvironment"]
old-location: rm\drminitenvironment.htm
tech.root: rm
ms.assetid: b46277f4-e854-4590-847a-cf4f878bee70
ms.date: 12/05/2018
ms.keywords: DRMInitEnvironment, DRMInitEnvironment function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMInitEnvironment, rm.drminitenvironment
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
 - DRMInitEnvironment
 - msdrm/DRMInitEnvironment
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
 - DRMInitEnvironment
---

# DRMInitEnvironment function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll 
    is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, 
    Windows 7, Windows Server 2012, and Windows 8. It may be altered or 
    unavailable in subsequent versions. Instead, use 
    <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 
    which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMInitEnvironment</b> function creates a 
    secure environment for all rights management calls.

## -parameters

### -param eSecurityProviderType [in]

Specifies the type of security provider to use.

### -param eSpecification [in]

Specifies which security provider to use.

### -param wszSecurityProvider [in]

The file name and ID of the security provider. A security provider can be a file on the computer (the 
      lockbox) or a hardware device that holds the secure machine key. The path to this key is obtained by calling 
      <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsecurityprovider">DRMGetSecurityProvider</a>.

### -param wszManifestCredentials [in]

A signed XrML structure that specifies conditions on the environment. For information about making a 
      manifest, see 
      <a href="/previous-versions/windows/desktop/adrms_sdk/creating-an-application-manifest">Creating an Application Manifest</a>.

### -param wszMachineCredentials [in]

The machine certificate.

### -param phEnv [out]

A pointer to an environment handle. Close the handle by calling 
      <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcloseenvironmenthandle">DRMCloseEnvironmentHandle</a>.

### -param phDefaultLibrary [out]

A pointer to the handle of the library used to create the principal object. You must close this handle 
      before closing the environment handle. For more information, see the Remarks section. Close by calling 
      <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. 
       Possible values include, but are not limited to, those in the following list. For a list of common error codes, 
       see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function loads the lockbox, and makes sure that only legal DLLs are loaded, according to the manifest.

The order of certificates is from least trusted first to most trusted (closest to the root) last.

When closing the handles returned by this function, close the library handle before closing the environment 
     handle. Otherwise, you will receive an <b>E_DRM_ENV_NOT_LOADED</b> error. Close the library 
     handle by calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a>. Close the environment 
     handle by calling 
     <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcloseenvironmenthandle">DRMCloseEnvironmentHandle</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>