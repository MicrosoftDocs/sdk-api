---
UID: NF:msdrm.DRMRegisterContent
title: DRMRegisterContent function (msdrm.h)
description: Informs the Active Directory Rights Management Services (AD RMS) client that an AD RMS-protected document is being or is no longer being displayed.
helpviewer_keywords: ["DRMRegisterContent","DRMRegisterContent function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMRegisterContent","rm.drmregistercontent"]
old-location: rm\drmregistercontent.htm
tech.root: rm
ms.assetid: ddf1ef8d-f509-43c0-87bd-9ea393a7231a
ms.date: 12/05/2018
ms.keywords: DRMRegisterContent, DRMRegisterContent function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRegisterContent, rm.drmregistercontent
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
 - DRMRegisterContent
 - msdrm/DRMRegisterContent
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
 - DRMRegisterContent
---

# DRMRegisterContent function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRegisterContent</b> function informs the Active Directory Rights Management Services (AD RMS) client that an AD RMS-protected document is being or is no longer being displayed.

## -parameters

### -param fRegister [in]

Pass <b>TRUE</b> when you open an AD RMS-protected document. Pass <b>FALSE</b> when you close that document.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function allows the AD RMS client to keep a reference count of all open AD RMS-protected documents in the client application. The AD RMS client uses this information to implement additional user interface security measures, such as disabling the print screen functionality, to prevent the protected documents from being accessed in an unauthorized manner. When the reference count is greater than zero, the additional user interface security measures are applied to all applications, not just those hosting the AD RMS-protected documents. Using this function is not required, but using it enables an application to obtain additional user interface security features for greater document security.

Every call to this function with <b>TRUE</b> must have a corresponding call to this function with <b>FALSE</b> to maintain proper reference counting.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>