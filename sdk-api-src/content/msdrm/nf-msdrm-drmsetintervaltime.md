---
UID: NF:msdrm.DRMSetIntervalTime
title: DRMSetIntervalTime function (msdrm.h)
description: Specifies the number of days from issuance that can pass before an end—user license must be renewed.
helpviewer_keywords: ["DRMSetIntervalTime","DRMSetIntervalTime function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetIntervalTime","rm.drmsetintervaltime"]
old-location: rm\drmsetintervaltime.htm
tech.root: rm
ms.assetid: b3b7af75-ed94-4c2f-abb2-95194796771c
ms.date: 12/05/2018
ms.keywords: DRMSetIntervalTime, DRMSetIntervalTime function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetIntervalTime, rm.drmsetintervaltime
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
 - DRMSetIntervalTime
 - msdrm/DRMSetIntervalTime
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
 - DRMSetIntervalTime
---

# DRMSetIntervalTime function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetIntervalTime</b> function specifies the number of days from issuance that can pass before an end–user license must be renewed. This value is specified in an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license in which to  set the interval time.

### -param cDays [in]

An unsigned integer  value that specifies the interval period, in days. For example, if you specify 30, the end–user license must be renewed within 30 days of the day  it was issued.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetintervaltime">DRMGetIntervalTime</a>