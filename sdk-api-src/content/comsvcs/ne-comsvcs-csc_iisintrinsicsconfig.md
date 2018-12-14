---
UID: NE:comsvcs.tagCSC_IISIntrinsicsConfig
title: CSC_IISIntrinsicsConfig
author: windows-sdk-content
description: Indicates whether the current IIS intrinsics are propagated into the new context.
old-location: cos\csc_iisintrinsicsconfig.htm
tech.root: cossdk
ms.assetid: 69a3989b-724c-4e32-8a6a-4892610b0118
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CSC_IISIntrinsicsConfig, CSC_IISIntrinsicsConfig enumeration [COM+], CSC_InheritIISIntrinsics, CSC_NoIISIntrinsics, _cos_CSC_IISIntrinsicsConfig, comsvcs/CSC_IISIntrinsicsConfig, comsvcs/CSC_InheritIISIntrinsics, comsvcs/CSC_NoIISIntrinsics, cos.csc_iisintrinsicsconfig
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
 - CSC_IISIntrinsicsConfig
product: Windows
targetos: Windows
req.typenames: CSC_IISIntrinsicsConfig
req.redist: 
---

# CSC_IISIntrinsicsConfig enumeration


## -description


Indicates whether the current IIS intrinsics are propagated into the new context.


## -enum-fields




### -field CSC_NoIISIntrinsics

The current IIS intrinsics do not propagate to the new context. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritIISIntrinsics

The current IIS intrinsics propagate to the new context. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.


## -remarks



This enumeration is used to configure the IIS intrinsics settings through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/458bd0d6-ed4f-45c2-8a96-1a4a08aad509">IServiceIISIntrinsicsConfig::IISIntrinsicsConfig</a>
 

 

