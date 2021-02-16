---
UID: NS:waasapitypes.tagOSUpdateAssessment
title: OSUpdateAssessment (waasapitypes.h)
description: The OSUpdateAssessment structure defines how up-to-date the OS on a targeted device is.
helpviewer_keywords: ["OSUpdateAssessment","OSUpdateAssessment structure","base.osupdateassessment","waasapitypes/OSUpdateAssessment"]
old-location: base\osupdateassessment.htm
tech.root: winprog
ms.assetid: D76D0587-E31E-48D2-9DF6-33444E4CA325
ms.date: 12/05/2018
ms.keywords: OSUpdateAssessment, OSUpdateAssessment structure, base.osupdateassessment, waasapitypes/OSUpdateAssessment
req.header: waasapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WaaSAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OSUpdateAssessment
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOSUpdateAssessment
 - waasapitypes/tagOSUpdateAssessment
 - OSUpdateAssessment
 - waasapitypes/OSUpdateAssessment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - waasapitypes.h
api_name:
 - OSUpdateAssessment
---

# OSUpdateAssessment structure


## -description

The <b>OSUpdateAssessment</b> structure defines how up-to-date the OS on a targeted device is. This structure is used primarily as a return value by <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a>, in order to retrieve an OS assessment in a single structure.

## -struct-fields

### -field isEndOfSupport

<b>true</b> if the OS on the device is no longer supported by Microsoft and will no longer receive servicing updates; otherwise, <b>false</b>.

### -field assessmentForCurrent

An <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a> structure containing an assessment against the latest update Microsoft has released.

### -field assessmentForUpToDate

An <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a> structure containing an assessment against the latest applicable quality update for the device.

### -field securityStatus

An <a href="/windows/desktop/SysInfo/updateassessmentstatus">UpdateAssessmentStatus</a> enumeration that details whether the device is on the latest applicable security update.

### -field assessmentTime

Timestamp when the assessment was done.

### -field releaseInfoTime

Timestamp when the release information was updated.

### -field currentOSBuild

The latest OS build that Microsoft has released. This value is used to determine whether a device is current.

### -field currentOSReleaseTime

The published timestamp of the release date for current OS build.

### -field upToDateOSBuild

The latest applicable OS build in the device's servicing train. This value is used to determine whether a device is up-to-date.

### -field upToDateOSReleaseTime

The published timestamp of the release date for the up-to-date OS build.