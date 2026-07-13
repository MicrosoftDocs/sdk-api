---
UID: NF:dsgetdc.DsGetSiteNameW
title: DsGetSiteNameW function (dsgetdc.h)
description: The DsGetSiteName function returns the name of the site where a computer resides. (Unicode)
helpviewer_keywords: ["DsGetSiteName", "DsGetSiteName function [Active Directory]", "DsGetSiteNameW", "_glines_dsgetsitename", "ad.dsgetsitename", "dsgetdc/DsGetSiteName", "dsgetdc/DsGetSiteNameW"]
old-location: ad\dsgetsitename.htm
tech.root: ad
ms.assetid: 2dfffd9a-af4f-4a93-8b3c-966e4f7c455f
ms.date: 12/05/2018
ms.keywords: DsGetSiteName, DsGetSiteName function [Active Directory], DsGetSiteNameA, DsGetSiteNameW, _glines_dsgetsitename, ad.dsgetsitename, dsgetdc/DsGetSiteName, dsgetdc/DsGetSiteNameA, dsgetdc/DsGetSiteNameW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetSiteNameW (Unicode) and DsGetSiteNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsGetSiteNameW
 - dsgetdc/DsGetSiteNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsGetSiteName
 - DsGetSiteNameA
 - DsGetSiteNameW
---

# DsGetSiteNameW function


## -description

The <b>DsGetSiteName</b> function returns the name of the site where a computer resides. For a domain controller (DC), the name of the site is the location of the configured DC. For a member workstation or member server, the name specifies the workstation site as configured in the domain of the computer.

## -parameters

### -param ComputerName [in]

Pointer to a null-terminated string that specifies the name of the server to send this function. A <b>NULL</b> implies the local computer.

### -param SiteName [out]

Pointer to a variable that receives a pointer to a null-terminated string specifying the site location of this computer. This string is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

## -returns

If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.

## -remarks

The <b>DsGetSiteName</b> function does not require any particular access to the specified domain. The function is sent to the "NetLogon" service on the computer specified by <i>ComputerName</i>.





> [!NOTE]
> The dsgetdc.h header defines DsGetSiteName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea">DsValidateSubnetName</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>
