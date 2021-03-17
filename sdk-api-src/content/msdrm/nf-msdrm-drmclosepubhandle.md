---
UID: NF:msdrm.DRMClosePubHandle
title: DRMClosePubHandle function (msdrm.h)
description: Closes a previously created DRMPUBHANDLE.
helpviewer_keywords: ["DRMClosePubHandle","DRMClosePubHandle function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMClosePubHandle","rm.drmclosepubhandle"]
old-location: rm\drmclosepubhandle.htm
tech.root: rm
ms.assetid: a263a1a8-01b8-4ca6-aefb-f4374459c0c0
ms.date: 12/05/2018
ms.keywords: DRMClosePubHandle, DRMClosePubHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMClosePubHandle, rm.drmclosepubhandle
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
 - DRMClosePubHandle
 - msdrm/DRMClosePubHandle
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
 - DRMClosePubHandle
---

# DRMClosePubHandle function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMClosePubHandle</b> function closes a previously created <b>DRMPUBHANDLE</b>.

## -parameters

### -param hPub [in]

A handle to a publishing object.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A <b>DRMPUBHANDLE</b> provides an opaque handle to many publishing objects. Creating, copying, and closing these handles with the appropriate Active Directory Rights Management function allows the AD RMS system to maintain a reference count on resources and free them appropriately, and also clears sensitive data from memory.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-handles-and-sessions">AD RMS Handles and Sessions</a>