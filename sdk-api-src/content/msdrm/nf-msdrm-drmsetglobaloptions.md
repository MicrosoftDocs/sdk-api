---
UID: NF:msdrm.DRMSetGlobalOptions
title: DRMSetGlobalOptions function (msdrm.h)
description: Sets the transport protocol to a specified value and optionally specifies whether the server lockbox is used.
helpviewer_keywords: ["DRMSetGlobalOptions","DRMSetGlobalOptions function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetGlobalOptions","rm.drmsetglobaloptions"]
old-location: rm\drmsetglobaloptions.htm
tech.root: rm
ms.assetid: fff0d503-e342-4f50-810c-bda4e9e14ad7
ms.date: 12/05/2018
ms.keywords: DRMSetGlobalOptions, DRMSetGlobalOptions function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetGlobalOptions, rm.drmsetglobaloptions
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
 - DRMSetGlobalOptions
 - msdrm/DRMSetGlobalOptions
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
 - DRMSetGlobalOptions
---

# DRMSetGlobalOptions function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetGlobalOptions</b> function sets the transport protocol to a specified value and optionally specifies whether the server lockbox is used.

## -parameters

### -param eGlobalOptions [in]

A value of the <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drmglobaloptions">DRMGLOBALOPTIONS</a> enumeration that specifies the option to set.

Only one option can be specified in each call to <b>DRMSetGlobalOptions</b>. For example, if both WinHTTP and the server lockbox are required, you must call <b>DRMSetGlobalOptions</b> twice, once with <i>eGlobalOptions</i> set to <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> and once with <i>eGlobalOptions</i> set to <b>DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR</b>.

### -param pvdata [in]

A pointer to a <b>void</b> value. This parameter is not currently used.

### -param dwlen [in]

The size, in bytes, of the <i>pvdata</i> buffer. This parameter is not currently used.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Applications cannot toggle between the WinHTTP and WinINet protocols.

WinINet does not support usage under the network service account. If an application will be run under the network service account, the application must specify the <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> option.

An AD RMS-enabled server application should call the <b>DRMSetGlobalOptions</b> function prior to calling any other rights management functions. Calling <b>DRMSetGlobalOptions</b> after other rights management functions have been called will not change the type of lockbox or transport protocol in use.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drmglobaloptions">DRMGLOBALOPTIONS</a>