---
UID: NS:comsvcs._ComponentHangMonitorInfo
title: "_ComponentHangMonitorInfo"
author: windows-sdk-content
description: Represents the hang monitoring configuration for a COM+ component.
old-location: cos\componenthangmonitorinfo.htm
old-project: cossdk
ms.assetid: 062b7bcf-e9b2-4024-ba9c-700cc7d69963
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ComponentHangMonitorInfo, ComponentHangMonitorInfo structure [COM+], _ComponentHangMonitorInfo, comsvcs/ComponentHangMonitorInfo, cos.componenthangmonitorinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: ComponentHangMonitorInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ComponentHangMonitorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ComponentHangMonitorInfo structure


## -description


Represents the hang monitoring configuration for a COM+ component.


## -struct-fields




### -field IsMonitored

Indicates whether the component is configured for hang monitoring.


### -field TerminateOnHang

Indicates whether the hang monitoring configuration for the component specifies the process will be terminated on a hang. This member is meaningful only if <b>IsMonitored</b> is <b>TRUE</b>.


### -field AvgCallThresholdInMs

The average call response time threshold configured for the component. This member is meaningful only if <b>IsMonitored</b> is <b>TRUE</b>.


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

