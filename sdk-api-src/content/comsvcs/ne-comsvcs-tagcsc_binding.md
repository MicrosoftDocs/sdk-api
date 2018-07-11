---
UID: NE:comsvcs.tagCSC_Binding
title: tagCSC_Binding
author: windows-sdk-content
description: Indicates whether all of the work that is submitted via the activity returned from CoCreateActivity should be bound to only one single-threaded apartment (STA). This enumeration has no impact on the multithreaded apartment (MTA).
old-location: cos\csc_binding.htm
old-project: cossdk
ms.assetid: 9267b4f1-96d1-4367-8114-3db43755ffed
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: CSC_BindToPoolThread, CSC_Binding, CSC_Binding enumeration [COM+], CSC_NoBinding, _cos_CSC_Binding, comsvcs/CSC_BindToPoolThread, comsvcs/CSC_Binding, comsvcs/CSC_NoBinding, cos.csc_binding, tagCSC_Binding
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CSC_Binding
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_Binding
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCSC_Binding enumeration


## -description


Indicates whether all of the work that is submitted via the activity returned from <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> should be bound to only one single-threaded apartment (STA). This enumeration has no impact on the multithreaded apartment (MTA).


## -enum-fields




### -field CSC_NoBinding

The work submitted through the activity is not bound to a single STA.


### -field CSC_BindToPoolThread

The work submitted through the activity is bound to a single STA.


## -remarks



Binding all of the work submitted through the activity to a single STA involves a trade-off between avoiding the need to marshal interfaces to components used by many of the different bits of work versus needing to synchronize on a specific STA.

This enumeration is used only to set the thread pool binding for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when calling <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. An error is returned if you try to set the thread pool binding when calling <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>. The values of this enumeration have no impact upon the MTA.




## -see-also




<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/9d2c4e6f-aa12-4874-a8e0-ca21a981b43f">IServiceThreadPoolConfig::SetBindingInfo</a>
 

 

