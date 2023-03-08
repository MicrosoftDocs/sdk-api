---
UID: NF:msdrm.DRMRepair
title: DRMRepair function (msdrm.h)
description: Repairs a client machine by deleting certificates previously created for the machine or user.
helpviewer_keywords: ["DRMRepair","DRMRepair function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMRepair","rm.drmrepair"]
old-location: rm\drmrepair.htm
tech.root: rm
ms.assetid: d3abebcd-1200-417c-a0ec-64768b3c320a
ms.date: 12/05/2018
ms.keywords: DRMRepair, DRMRepair function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRepair, rm.drmrepair
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
 - DRMRepair
 - msdrm/DRMRepair
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
 - DRMRepair
---

# DRMRepair function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRepair</b> function repairs a client machine by deleting certificates previously created for the machine or user.



## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>DRMRepair</b> function first determines whether the machine is activated. If the machine activation is not valid, then the <b>DRMRepair</b> function will restore the machine to a clean state by deleting the machine certificate, rights account certificate, and client licensor certificate of the  currently logged on user.

If the machine activation is valid but the rights account certificate is not valid, then the <b>DRMRepair</b> function will delete the rights account certificate and client licensor certificate of the  currently logged on user.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetglobaloptions">DRMSetGlobalOptions</a>
