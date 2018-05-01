---
UID: NF:comsvcs.IServiceThreadPoolConfig.SetBindingInfo
title: IServiceThreadPoolConfig::SetBindingInfo method
author: windows-driver-content
description: Binds all work submitted by the activity to a single single-threaded apartment.
old-location: cos\iservicethreadpoolconfig_setbindinginfo.htm
old-project: cossdk
ms.assetid: 9d2c4e6f-aa12-4874-a8e0-ca21a981b43f
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IServiceThreadPoolConfig, IServiceThreadPoolConfig interface [COM+], SetBindingInfo method, IServiceThreadPoolConfig::SetBindingInfo, SetBindingInfo method [COM+], SetBindingInfo method [COM+], IServiceThreadPoolConfig interface, SetBindingInfo,IServiceThreadPoolConfig.SetBindingInfo, _cos_IServiceThreadPoolConfig_SetBindingInfo, comsvcs/IServiceThreadPoolConfig::SetBindingInfo, cos.iservicethreadpoolconfig_setbindinginfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceThreadPoolConfig.SetBindingInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceThreadPoolConfig::SetBindingInfo method


## -description


Binds all work submitted by the activity to a single single-threaded apartment.


## -parameters




### -param binding [in]

A value from the <a href="https://msdn.microsoft.com/9267b4f1-96d1-4367-8114-3db43755ffed">CSC_Binding</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf">IServiceThreadPoolConfig</a>
 

 

