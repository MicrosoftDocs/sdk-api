---
UID: NE:comsvcs.tagCSC_Binding
title: CSC_Binding (comsvcs.h)
description: Indicates whether all of the work that is submitted via the activity returned from CoCreateActivity should be bound to only one single-threaded apartment (STA). This enumeration has no impact on the multithreaded apartment (MTA).
helpviewer_keywords: ["CSC_BindToPoolThread","CSC_Binding","CSC_Binding enumeration [COM+]","CSC_NoBinding","_cos_CSC_Binding","comsvcs/CSC_BindToPoolThread","comsvcs/CSC_Binding","comsvcs/CSC_NoBinding","cos.csc_binding"]
old-location: cos\csc_binding.htm
tech.root: cos
ms.assetid: 9267b4f1-96d1-4367-8114-3db43755ffed
ms.date: 12/05/2018
ms.keywords: CSC_BindToPoolThread, CSC_Binding, CSC_Binding enumeration [COM+], CSC_NoBinding, _cos_CSC_Binding, comsvcs/CSC_BindToPoolThread, comsvcs/CSC_Binding, comsvcs/CSC_NoBinding, cos.csc_binding
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
req.typenames: CSC_Binding
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_Binding
 - comsvcs/tagCSC_Binding
 - CSC_Binding
 - comsvcs/CSC_Binding
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
 - CSC_Binding
---

# CSC_Binding enumeration


## -description

Indicates whether all of the work that is submitted via the activity returned from <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> should be bound to only one single-threaded apartment (STA). This enumeration has no impact on the multithreaded apartment (MTA).

## -enum-fields

### -field CSC_NoBinding:0

The work submitted through the activity is not bound to a single STA.

### -field CSC_BindToPoolThread

The work submitted through the activity is bound to a single STA.

## -remarks

Binding all of the work submitted through the activity to a single STA involves a trade-off between avoiding the need to marshal interfaces to components used by many of the different bits of work versus needing to synchronize on a specific STA.

This enumeration is used only to set the thread pool binding for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. An error is returned if you try to set the thread pool binding when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>. The values of this enumeration have no impact upon the MTA.

## -see-also

<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-setbindinginfo">IServiceThreadPoolConfig::SetBindingInfo</a>
