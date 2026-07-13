---
UID: NF:dsgetdc.DsGetDcSiteCoverageA
title: DsGetDcSiteCoverageA function (dsgetdc.h)
description: The DsGetDcSiteCoverage function returns the site names of all sites covered by a domain controller. (ANSI)
helpviewer_keywords: ["DsGetDcSiteCoverageA", "dsgetdc/DsGetDcSiteCoverageA"]
old-location: ad\dsgetdcsitecoverage.htm
tech.root: ad
ms.assetid: e0f757d9-36b6-40f8-a1db-fb5b9862b46a
ms.date: 12/05/2018
ms.keywords: DsGetDcSiteCoverage, DsGetDcSiteCoverage function [Active Directory], DsGetDcSiteCoverageA, DsGetDcSiteCoverageW, _glines_dsgetdcsitecoverage, ad.dsgetdcsitecoverage, dsgetdc/DsGetDcSiteCoverage, dsgetdc/DsGetDcSiteCoverageA, dsgetdc/DsGetDcSiteCoverageW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcSiteCoverageW (Unicode) and DsGetDcSiteCoverageA (ANSI)
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
 - DsGetDcSiteCoverageA
 - dsgetdc/DsGetDcSiteCoverageA
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
 - DsGetDcSiteCoverage
 - DsGetDcSiteCoverageA
 - DsGetDcSiteCoverageW
---

# DsGetDcSiteCoverageA function


## -description

The <b>DsGetDcSiteCoverage</b> function returns the site names of all sites covered by a domain controller.

## -parameters

### -param ServerName [in, optional]

The null-terminated string value that specifies the name of the remote domain controller.

### -param EntryCount [out]

Pointer to a <b>ULONG</b> value that receives  the number of sites covered by the domain controller.

### -param SiteNames [out]

Pointer to an array of pointers to null-terminated strings that receives the site names. To free the returned buffer, call the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

## -returns

This function returns DSGETDCAPI DWORD.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetsitenamea">DsGetSiteName</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DsGetDcSiteCoverage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
