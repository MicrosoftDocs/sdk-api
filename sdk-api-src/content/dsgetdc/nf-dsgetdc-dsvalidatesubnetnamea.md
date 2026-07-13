---
UID: NF:dsgetdc.DsValidateSubnetNameA
title: DsValidateSubnetNameA function (dsgetdc.h)
description: The DsValidateSubnetName function validates a subnet name in the form xxx.xxx.xxx.xxx/YY. (ANSI)
helpviewer_keywords: ["DsValidateSubnetNameA", "dsgetdc/DsValidateSubnetNameA"]
old-location: ad\dsvalidatesubnetname.htm
tech.root: ad
ms.assetid: bed49e08-4cb7-439c-bfb7-815263ec7568
ms.date: 12/05/2018
ms.keywords: DsValidateSubnetName, DsValidateSubnetName function [Active Directory], DsValidateSubnetNameA, DsValidateSubnetNameW, _glines_dsvalidatesubnetname, ad.dsvalidatesubnetname, dsgetdc/DsValidateSubnetName, dsgetdc/DsValidateSubnetNameA, dsgetdc/DsValidateSubnetNameW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsValidateSubnetNameW (Unicode) and DsValidateSubnetNameA (ANSI)
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
 - DsValidateSubnetNameA
 - dsgetdc/DsValidateSubnetNameA
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
 - DsValidateSubnetName
 - DsValidateSubnetNameA
 - DsValidateSubnetNameW
---

# DsValidateSubnetNameA function


## -description

The <b>DsValidateSubnetName</b> function validates a subnet name in the form xxx.xxx.xxx.xxx/YY. The Xxx.xxx.xxx.xxx portion must be a valid IP address. Yy must be the number of leftmost significant bits included in the mask. All bits of the IP address that are not covered by the mask must be specified as zero.

## -parameters

### -param SubnetName [in]

Pointer to a null-terminated string that specifies the name of the subnet to validate.

## -returns

If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is the following error code.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetsitenamea">DsGetSiteName</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DsValidateSubnetName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
