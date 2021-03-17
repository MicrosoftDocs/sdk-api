---
UID: NF:msdrm.DRMCreateEnablingPrincipal
title: DRMCreateEnablingPrincipal function (msdrm.h)
description: Creates an enabling principal needed to bind to a license.
helpviewer_keywords: ["DRMCreateEnablingPrincipal","DRMCreateEnablingPrincipal function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateEnablingPrincipal","rm.drmcreateenablingprincipal"]
old-location: rm\drmcreateenablingprincipal.htm
tech.root: rm
ms.assetid: 92858a46-cef5-4d25-9f3c-cbb343743565
ms.date: 12/05/2018
ms.keywords: DRMCreateEnablingPrincipal, DRMCreateEnablingPrincipal function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingPrincipal, rm.drmcreateenablingprincipal
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
 - DRMCreateEnablingPrincipal
 - msdrm/DRMCreateEnablingPrincipal
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
 - DRMCreateEnablingPrincipal
---

# DRMCreateEnablingPrincipal function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingPrincipal</b> function creates an enabling principal needed to bind to a license.

## -parameters

### -param hEnv [in]

A handle to an environment created by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param hLibrary [in]

A handle to a library. Currently, the only valid library that can be used is the one passed out by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param wszObject [in]

A pointer to a null-terminated Unicode string that specifies the enabling principal type. An application can use the object constants specified in Msdrmgetinfo.h.

### -param pidPrincipal [in]

A pointer to a <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmid">DRMID</a> structure that identifies the enabling principal. The <b>DRMID</b> members can be <b>NULL</b> to use the first principal in a license.

### -param wszCredentials [in]

A pointer to a null-terminated Unicode string that contains the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> of the current user.

### -param phEnablingPrincipal [out]

A pointer to a <b>DRMHANDLE</b> value that receives the created principal. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The enabling principal this function creates is used in the <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a> structure passed into <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the enabling principal handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>