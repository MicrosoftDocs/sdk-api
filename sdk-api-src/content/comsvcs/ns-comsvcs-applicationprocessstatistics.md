---
UID: NS:comsvcs._ApplicationProcessStatistics
title: ApplicationProcessStatistics (comsvcs.h)
description: Represents statistical information about a process hosting COM+ applications.
helpviewer_keywords: ["ApplicationProcessStatistics","ApplicationProcessStatistics structure [COM+]","comsvcs/ApplicationProcessStatistics","cos.applicationprocessstatistics"]
old-location: cos\applicationprocessstatistics.htm
tech.root: cos
ms.assetid: 7ce16cef-baa4-491c-89e7-f6283e1a646f
ms.date: 12/05/2018
ms.keywords: ApplicationProcessStatistics, ApplicationProcessStatistics structure [COM+], comsvcs/ApplicationProcessStatistics, cos.applicationprocessstatistics
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
req.typenames: ApplicationProcessStatistics
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ApplicationProcessStatistics
 - comsvcs/_ApplicationProcessStatistics
 - ApplicationProcessStatistics
 - comsvcs/ApplicationProcessStatistics
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
 - ApplicationProcessStatistics
---

# ApplicationProcessStatistics structure


## -description

Represents statistical information about a process hosting COM+ applications.

## -struct-fields

### -field NumCallsOutstanding

The number of calls currently outstanding in tracked components in the process.

### -field NumTrackedComponents

The number of distinct tracked components instantiated in the process.

### -field NumComponentInstances

The number of component instances in the process.

### -field AvgCallsPerSecond

A rolling average of the number of calls this process is servicing per second.

### -field Reserved1

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved2

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved3

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved4

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>