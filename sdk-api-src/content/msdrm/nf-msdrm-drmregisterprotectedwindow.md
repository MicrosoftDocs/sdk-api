---
UID: NF:msdrm.DRMRegisterProtectedWindow
title: DRMRegisterProtectedWindow function (msdrm.h)
description: Registers a window in the protected environment.
helpviewer_keywords: ["DRMRegisterProtectedWindow","DRMRegisterProtectedWindow function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMRegisterProtectedWindow","rm.drmregisterprotectedwindow"]
old-location: rm\drmregisterprotectedwindow.htm
tech.root: rm
ms.assetid: 4801ea8b-4437-4c2b-bec0-60aefaaa1251
ms.date: 12/05/2018
ms.keywords: DRMRegisterProtectedWindow, DRMRegisterProtectedWindow function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRegisterProtectedWindow, rm.drmregisterprotectedwindow
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
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
ms.custom: 19H1
f1_keywords:
 - DRMRegisterProtectedWindow
 - msdrm/DRMRegisterProtectedWindow
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
 - DRMRegisterProtectedWindow
---

# DRMRegisterProtectedWindow function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRegisterProtectedWindow</b> function registers a window in the protected environment.

## -parameters

### -param hEnv [in]

A handle to the secure environment.

### -param hwnd [in]

A handle to the window to be registered.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If the process ID does not equal the ID of the thread that created the window, the function fails. Also, if the visibility state of the window is not <b>WS_VISIBLE</b>, the function fails.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>