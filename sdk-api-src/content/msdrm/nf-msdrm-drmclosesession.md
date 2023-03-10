---
UID: NF:msdrm.DRMCloseSession
title: DRMCloseSession function (msdrm.h)
description: Closes a client session or a license storage session.
helpviewer_keywords: ["DRMCloseSession","DRMCloseSession function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCloseSession","rm.drmclosesession"]
old-location: rm\drmclosesession.htm
tech.root: rm
ms.assetid: e948b31f-382c-4a32-8cc3-98df8c4a6db0
ms.date: 12/05/2018
ms.keywords: DRMCloseSession, DRMCloseSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseSession, rm.drmclosesession
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
req.product: Rights Management Services client 1.0 SP2  or later
ms.custom: 19H1
f1_keywords:
 - DRMCloseSession
 - msdrm/DRMCloseSession
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
 - DRMCloseSession
---

# DRMCloseSession function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseSession</b> function closes a client session or a license storage session.

## -parameters

### -param hSession [in]

A handle to the session to be closed.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Client sessions are created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function. License storage sessions are created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> function. Be sure to close a session properly by using this function, which clears out sensitive information from memory and properly closes session handles.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/activating-a-computer">Activating a Computer</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a>