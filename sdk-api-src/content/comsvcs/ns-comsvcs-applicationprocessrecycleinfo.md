---
UID: NS:comsvcs._ApplicationProcessRecycleInfo
title: ApplicationProcessRecycleInfo (comsvcs.h)
description: Represents details about the recycling of a process hosting COM+ applications.
helpviewer_keywords: ["ApplicationProcessRecycleInfo","ApplicationProcessRecycleInfo structure [COM+]","comsvcs/ApplicationProcessRecycleInfo","cos.applicationprocessrecycleinfo"]
old-location: cos\applicationprocessrecycleinfo.htm
tech.root: cos
ms.assetid: 9e00c6a3-b82e-48a2-bec5-c5fbd6960072
ms.date: 12/05/2018
ms.keywords: ApplicationProcessRecycleInfo, ApplicationProcessRecycleInfo structure [COM+], comsvcs/ApplicationProcessRecycleInfo, cos.applicationprocessrecycleinfo
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
req.typenames: ApplicationProcessRecycleInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ApplicationProcessRecycleInfo
 - comsvcs/_ApplicationProcessRecycleInfo
 - ApplicationProcessRecycleInfo
 - comsvcs/ApplicationProcessRecycleInfo
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
 - ApplicationProcessRecycleInfo
---

# ApplicationProcessRecycleInfo structure


## -description

Represents details about the recycling of a process hosting COM+ applications.

## -struct-fields

### -field IsRecyclable

Indicates whether the process is one that can be recycled. For example, only COM+ server applications can be recycled, and applications running as Windows services cannot be recycled.

### -field IsRecycled

Indicates whether the process is a COM+ server application instance that has been recycled.

### -field TimeRecycled

The time at which the process was recycled. This member is meaningful only if <b>IsRecycled</b> is <b>TRUE</b>.

### -field TimeToTerminate

The time at which a recycled process will be forcibly terminated if it does not shut down on its own before this time. This member is meaningful only if <b>IsRecycled</b> is <b>TRUE</b>.

### -field RecycleReasonCode

A code that indicates the reason a process was recycled. This is usually one of the recycle reason code constants defined in Comsvcs.h (for example, CRR_RECYCLED_FROM_UI), but may be any code supplied by an administrative application in a call to <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-recycleapplicationinstances">ICOMAdminCatalog2::RecycleApplicationInstances</a>. This member is meaningful only if <b>IsRecycled</b> is <b>TRUE</b>.

### -field IsPendingRecycle

Indicates whether a paused COM+ server application instance has met the conditions for automatic recycling. If so, the application instance will be recycled when it is resumed.

### -field HasAutomaticLifetimeRecycling

Indicates whether the process is an instance of a COM+ server application that has been configured for automatic recycling based on lifetime.

### -field TimeForAutomaticRecycling

The time at which the process will be automatically recycled. This member is meaningful only if <b>HasAutomaticLifetimeRecycling</b> is <b>TRUE</b>.

### -field MemoryLimitInKB

The recycling memory limit configured for a COM+ server application in kilobytes, or 0 if the application is not configured for automatic recycling based on memory usage.

### -field MemoryUsageInKBLastCheck

The memory usage of the process in kilobytes the last time this metric was calculated by the Tracker Server. This is set to DATA_NOT_AVAILABLE (0xFFFFFFFF) if the application is not configured for automatic recycling based on memory usage, or if memory usage has not yet been checked.

### -field ActivationLimit

The activation limit configured for a COM+ server application, or 0 if the application is not configured for automatic recycling based on activation count. This data is not currently available, and is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field NumActivationsLastReported

The total number of activations performed in a COM+ server application instance, or 0 if the process is not hosting a COM+ server application. This data is not currently available, and is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field CallLimit

The call limit configured for a COM+ server application, or zero if the application is not configured for automatic recycling based on number of calls. This data is not currently available, and is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field NumCallsLastReported

The total number of calls serviced by a COM+ server application instance, or 0 if the process is not hosting a COM+ server application. This data is not currently available, and is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>