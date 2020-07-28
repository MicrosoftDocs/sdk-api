---
UID: NE:comsvcs.tagCSC_COMTIIntrinsicsConfig
title: CSC_COMTIIntrinsicsConfig (comsvcs.h)
description: Indicates whether the current COM Transaction Integrator (COMTI) intrinsics are propagated into the new context.
helpviewer_keywords: ["CSC_COMTIIntrinsicsConfig","CSC_COMTIIntrinsicsConfig enumeration [COM+]","CSC_InheritCOMTIIntrinsics","CSC_NoCOMTIIntrinsics","_cos_CSC_COMTIIntrinsicsConfig","comsvcs/CSC_COMTIIntrinsicsConfig","comsvcs/CSC_InheritCOMTIIntrinsics","comsvcs/CSC_NoCOMTIIntrinsics","cos.csc_comtiintrinsicsconfig"]
old-location: cos\csc_comtiintrinsicsconfig.htm
tech.root: cos
ms.assetid: 0d700648-b5fe-46f6-9d27-e2601fe88d71
ms.date: 12/05/2018
ms.keywords: CSC_COMTIIntrinsicsConfig, CSC_COMTIIntrinsicsConfig enumeration [COM+], CSC_InheritCOMTIIntrinsics, CSC_NoCOMTIIntrinsics, _cos_CSC_COMTIIntrinsicsConfig, comsvcs/CSC_COMTIIntrinsicsConfig, comsvcs/CSC_InheritCOMTIIntrinsics, comsvcs/CSC_NoCOMTIIntrinsics, cos.csc_comtiintrinsicsconfig
f1_keywords:
- comsvcs/CSC_COMTIIntrinsicsConfig
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ComSvcs.h
api_name:
- CSC_COMTIIntrinsicsConfig
targetos: Windows
req.typenames: CSC_COMTIIntrinsicsConfig
req.redist: 
ms.custom: 19H1
---

# CSC_COMTIIntrinsicsConfig enumeration


## -description


Indicates whether the current COM Transaction Integrator (COMTI) intrinsics are propagated into the new context. Values from this enumeration are passed to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicecomtiintrinsicsconfig-comtiintrinsicsconfig">IServiceComTIIntrinsicsConfig::ComTIIntrinsicsConfig</a>. The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.


## -enum-fields




### -field CSC_NoCOMTIIntrinsics

The current COMTI intrinsics do not propagate to the new context. This is the default setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritCOMTIIntrinsics

The current COMTI intrinsics propagate to the new context. This is the default setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.



## -remarks



This enumeration is used to configure the COMTI intrinsics settings through <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicecomtiintrinsicsconfig-comtiintrinsicsconfig">IServiceComTIIntrinsicsConfig::ComTIIntrinsicsConfig</a>
 

 

