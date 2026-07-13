---
UID: NF:msdrm.DRMGetIntervalTime
title: DRMGetIntervalTime function (msdrm.h)
description: Retrieves the number of days from issuance that can pass before an end—user license must be renewed.
helpviewer_keywords: ["DRMGetIntervalTime","DRMGetIntervalTime function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetIntervalTime","rm.drmgetintervaltime"]
old-location: rm\drmgetintervaltime.htm
tech.root: rm
ms.assetid: 681791b1-caeb-46ef-8cae-c93d46a6729e
ms.date: 12/05/2018
ms.keywords: DRMGetIntervalTime, DRMGetIntervalTime function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetIntervalTime, rm.drmgetintervaltime
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
 - DRMGetIntervalTime
 - msdrm/DRMGetIntervalTime
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
 - DRMGetIntervalTime
---

# DRMGetIntervalTime function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetIntervalTime</b> function retrieves the number of days from issuance that can pass before an end–user license must be renewed. This value is retrieved from an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license from which the interval time can be retrieved.

### -param pcDays [in]

A pointer to a <b>UINT</b> that specifies the interval period, in days. For example, if the value is  30, the end–user license must be renewed within 30 days of the day  it was issued.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetintervaltime">DRMSetIntervalTime</a>