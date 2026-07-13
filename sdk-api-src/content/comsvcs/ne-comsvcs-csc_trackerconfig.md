---
UID: NE:comsvcs.tagCSC_TrackerConfig
title: CSC_TrackerConfig (comsvcs.h)
description: Indicates whether the tracker property is added to the context in which the enclosed code runs.
helpviewer_keywords: ["CSC_DontUseTracker","CSC_TrackerConfig","CSC_TrackerConfig enumeration [COM+]","CSC_UseTracker","_cos_CSC_TrackerConfig","comsvcs/CSC_DontUseTracker","comsvcs/CSC_TrackerConfig","comsvcs/CSC_UseTracker","cos.csc_trackerconfig"]
old-location: cos\csc_trackerconfig.htm
tech.root: cos
ms.assetid: 48f01634-9802-4824-b251-ccb6e71aa099
ms.date: 12/05/2018
ms.keywords: CSC_DontUseTracker, CSC_TrackerConfig, CSC_TrackerConfig enumeration [COM+], CSC_UseTracker, _cos_CSC_TrackerConfig, comsvcs/CSC_DontUseTracker, comsvcs/CSC_TrackerConfig, comsvcs/CSC_UseTracker, cos.csc_trackerconfig
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
req.typenames: CSC_TrackerConfig
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_TrackerConfig
 - comsvcs/tagCSC_TrackerConfig
 - CSC_TrackerConfig
 - comsvcs/CSC_TrackerConfig
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
 - CSC_TrackerConfig
---

# CSC_TrackerConfig enumeration


## -description

Indicates whether the tracker property is added to the context in which the enclosed code runs.

## -enum-fields

### -field CSC_DontUseTracker:0

The tracker property is not added to the context in which the enclosed code runs.

### -field CSC_UseTracker

The tracker property is added to the context in which the enclosed code runs.

## -remarks

This enumeration is used to configure the tracker property through <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.

The tracker property is a reporting mechanism used by monitoring code to watch which code is running at a given time. It is the reporting mechanism behind the spinning balls in the Component Services administrative tool.

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicetrackerconfig-trackerconfig">IServiceTrackerConfig::TrackerConfig</a>
