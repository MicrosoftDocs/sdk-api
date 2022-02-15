---
UID: NE:comsvcs.tagCSC_IISIntrinsicsConfig
title: CSC_IISIntrinsicsConfig (comsvcs.h)
description: Indicates whether the current IIS intrinsics are propagated into the new context.
helpviewer_keywords: ["CSC_IISIntrinsicsConfig","CSC_IISIntrinsicsConfig enumeration [COM+]","CSC_InheritIISIntrinsics","CSC_NoIISIntrinsics","_cos_CSC_IISIntrinsicsConfig","comsvcs/CSC_IISIntrinsicsConfig","comsvcs/CSC_InheritIISIntrinsics","comsvcs/CSC_NoIISIntrinsics","cos.csc_iisintrinsicsconfig"]
old-location: cos\csc_iisintrinsicsconfig.htm
tech.root: cos
ms.assetid: 69a3989b-724c-4e32-8a6a-4892610b0118
ms.date: 12/05/2018
ms.keywords: CSC_IISIntrinsicsConfig, CSC_IISIntrinsicsConfig enumeration [COM+], CSC_InheritIISIntrinsics, CSC_NoIISIntrinsics, _cos_CSC_IISIntrinsicsConfig, comsvcs/CSC_IISIntrinsicsConfig, comsvcs/CSC_InheritIISIntrinsics, comsvcs/CSC_NoIISIntrinsics, cos.csc_iisintrinsicsconfig
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CSC_IISIntrinsicsConfig
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_IISIntrinsicsConfig
 - comsvcs/tagCSC_IISIntrinsicsConfig
 - CSC_IISIntrinsicsConfig
 - comsvcs/CSC_IISIntrinsicsConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_IISIntrinsicsConfig
---

# CSC_IISIntrinsicsConfig enumeration


## -description

Indicates whether the current IIS intrinsics are propagated into the new context.

## -enum-fields

### -field CSC_NoIISIntrinsics:0

The current IIS intrinsics do not propagate to the new context. This is the default setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.

### -field CSC_InheritIISIntrinsics

The current IIS intrinsics propagate to the new context. This is the default setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.

## -remarks

This enumeration is used to configure the IIS intrinsics settings through <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceiisintrinsicsconfig-iisintrinsicsconfig">IServiceIISIntrinsicsConfig::IISIntrinsicsConfig</a>
