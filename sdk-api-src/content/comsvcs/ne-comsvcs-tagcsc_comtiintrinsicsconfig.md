---
UID: NE:comsvcs.tagCSC_COMTIIntrinsicsConfig
title: tagCSC_COMTIIntrinsicsConfig
author: windows-driver-content
description: Indicates whether the current COM Transaction Integrator (COMTI) intrinsics are propagated into the new context.
old-location: cos\csc_comtiintrinsicsconfig.htm
old-project: cossdk
ms.assetid: 0d700648-b5fe-46f6-9d27-e2601fe88d71
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CSC_COMTIIntrinsicsConfig, CSC_COMTIIntrinsicsConfig enumeration [COM+], CSC_InheritCOMTIIntrinsics, CSC_NoCOMTIIntrinsics, _cos_CSC_COMTIIntrinsicsConfig, comsvcs/CSC_COMTIIntrinsicsConfig, comsvcs/CSC_InheritCOMTIIntrinsics, comsvcs/CSC_NoCOMTIIntrinsics, cos.csc_comtiintrinsicsconfig, tagCSC_COMTIIntrinsicsConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: CSC_COMTIIntrinsicsConfig
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ComSvcs.h
api_name:
-	CSC_COMTIIntrinsicsConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCSC_COMTIIntrinsicsConfig enumeration


## -description


Indicates whether the current COM Transaction Integrator (COMTI) intrinsics are propagated into the new context. Values from this enumeration are passed to <a href="https://msdn.microsoft.com/2e534123-6300-4da3-a220-ba0b41a7c9a2">IServiceComTIIntrinsicsConfig::ComTIIntrinsicsConfig</a>. The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.


## -enum-fields




### -field CSC_NoCOMTIIntrinsics

The current COMTI intrinsics do not propagate to the new context. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritCOMTIIntrinsics

The current COMTI intrinsics propagate to the new context. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.



## -remarks



This enumeration is used to configure the COMTI intrinsics settings through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.





## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/2e534123-6300-4da3-a220-ba0b41a7c9a2">IServiceComTIIntrinsicsConfig::ComTIIntrinsicsConfig</a>
 

 

