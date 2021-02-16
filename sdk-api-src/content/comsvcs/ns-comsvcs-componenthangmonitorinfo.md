---
UID: NS:comsvcs._ComponentHangMonitorInfo
title: ComponentHangMonitorInfo (comsvcs.h)
description: Represents the hang monitoring configuration for a COM+ component.
helpviewer_keywords: ["ComponentHangMonitorInfo","ComponentHangMonitorInfo structure [COM+]","comsvcs/ComponentHangMonitorInfo","cos.componenthangmonitorinfo"]
old-location: cos\componenthangmonitorinfo.htm
tech.root: cos
ms.assetid: 062b7bcf-e9b2-4024-ba9c-700cc7d69963
ms.date: 12/05/2018
ms.keywords: ComponentHangMonitorInfo, ComponentHangMonitorInfo structure [COM+], comsvcs/ComponentHangMonitorInfo, cos.componenthangmonitorinfo
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ComponentHangMonitorInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ComponentHangMonitorInfo
 - comsvcs/_ComponentHangMonitorInfo
 - ComponentHangMonitorInfo
 - comsvcs/ComponentHangMonitorInfo
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
 - ComponentHangMonitorInfo
---

# ComponentHangMonitorInfo structure


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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>