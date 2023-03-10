---
UID: NF:comsvcs.IServiceTrackerConfig.TrackerConfig
title: IServiceTrackerConfig::TrackerConfig (comsvcs.h)
description: Configures the tracker property for the enclosed work.
helpviewer_keywords: ["IServiceTrackerConfig interface [COM+]","TrackerConfig method","IServiceTrackerConfig.TrackerConfig","IServiceTrackerConfig::TrackerConfig","TrackerConfig","TrackerConfig method [COM+]","TrackerConfig method [COM+]","IServiceTrackerConfig interface","_cos_IServiceTrackerConfig_TrackerConfig","comsvcs/IServiceTrackerConfig::TrackerConfig","cos.iservicetrackerconfig_trackerconfig"]
old-location: cos\iservicetrackerconfig_trackerconfig.htm
tech.root: cos
ms.assetid: cdeb982b-720a-4d69-9c3c-d7a5a4527991
ms.date: 12/05/2018
ms.keywords: IServiceTrackerConfig interface [COM+],TrackerConfig method, IServiceTrackerConfig.TrackerConfig, IServiceTrackerConfig::TrackerConfig, TrackerConfig, TrackerConfig method [COM+], TrackerConfig method [COM+],IServiceTrackerConfig interface, _cos_IServiceTrackerConfig_TrackerConfig, comsvcs/IServiceTrackerConfig::TrackerConfig, cos.iservicetrackerconfig_trackerconfig
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceTrackerConfig::TrackerConfig
 - comsvcs/IServiceTrackerConfig::TrackerConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceTrackerConfig.TrackerConfig
---

# IServiceTrackerConfig::TrackerConfig


## -description

Configures the tracker property for the enclosed work.

## -parameters

### -param trackerConfig [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_trackerconfig">CSC_TrackerConfig</a> enumeration.

### -param szTrackerAppName [in]

The application identifier under which tracker information is reported.

### -param szTrackerCtxName [in]

The context name under which tracker information is reported.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

Because no component is associated with this tracker property, tracker activity is reported as arising from a component with the name specified by <i>szTrackerAppName</i>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetrackerconfig">IServiceTrackerConfig</a>