---
UID: NE:waasapitypes.tagUpdateAssessmentStatus
title: UpdateAssessmentStatus (waasapitypes.h)
description: Describes how up-to-date the OS on a device is.
helpviewer_keywords: ["UpdateAssessmentStatus","UpdateAssessmentStatus enumeration","UpdateAssessmentStatus_Latest","UpdateAssessmentStatus_NotLatestDeferredFeature","UpdateAssessmentStatus_NotLatestDeferredQuality","UpdateAssessmentStatus_NotLatestEndOfSupport","UpdateAssessmentStatus_NotLatestHardRestriction","UpdateAssessmentStatus_NotLatestManaged","UpdateAssessmentStatus_NotLatestPausedFeature","UpdateAssessmentStatus_NotLatestPausedQuality","UpdateAssessmentStatus_NotLatestServicingTrain","UpdateAssessmentStatus_NotLatestSoftRestriction","UpdateAssessmentStatus_NotLatestUnknown","UpdateAssessmentStatus_NotLatestTargetedVersion","base.updateassessmentstatus","waasapitypes/ UpdateAssessmentStatus_Latest","waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredFeature","waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredQuality","waasapitypes/ UpdateAssessmentStatus_NotLatestEndOfSupport","waasapitypes/ UpdateAssessmentStatus_NotLatestHardRestriction","waasapitypes/ UpdateAssessmentStatus_NotLatestManaged","waasapitypes/ UpdateAssessmentStatus_NotLatestPausedFeature","waasapitypes/ UpdateAssessmentStatus_NotLatestPausedQuality","waasapitypes/ UpdateAssessmentStatus_NotLatestServicingTrain","waasapitypes/ UpdateAssessmentStatus_NotLatestSoftRestriction","waasapitypes/ UpdateAssessmentStatus_NotLatestUnknown","waasapitypes/ UpdateAssessmentStatus_NotLatestTargetedVersion","waasapitypes/UpdateAssessmentStatus"]
old-location: base\updateassessmentstatus.htm
tech.root: winprog
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
ms.date: 12/05/2018
ms.keywords: UpdateAssessmentStatus, UpdateAssessmentStatus enumeration, UpdateAssessmentStatus_Latest, UpdateAssessmentStatus_NotLatestDeferredFeature, UpdateAssessmentStatus_NotLatestDeferredQuality, UpdateAssessmentStatus_NotLatestEndOfSupport, UpdateAssessmentStatus_NotLatestHardRestriction, UpdateAssessmentStatus_NotLatestManaged, UpdateAssessmentStatus_NotLatestPausedFeature, UpdateAssessmentStatus_NotLatestPausedQuality, UpdateAssessmentStatus_NotLatestServicingTrain, UpdateAssessmentStatus_NotLatestSoftRestriction, UpdateAssessmentStatus_NotLatestUnknown, UpdateAssessmentStatus_NotLatestTargetedVersion, base.updateassessmentstatus, waasapitypes/ UpdateAssessmentStatus_Latest, waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredFeature, waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredQuality, waasapitypes/ UpdateAssessmentStatus_NotLatestEndOfSupport, waasapitypes/ UpdateAssessmentStatus_NotLatestHardRestriction, waasapitypes/ UpdateAssessmentStatus_NotLatestManaged, waasapitypes/ UpdateAssessmentStatus_NotLatestPausedFeature, waasapitypes/ UpdateAssessmentStatus_NotLatestPausedQuality, waasapitypes/ UpdateAssessmentStatus_NotLatestServicingTrain, waasapitypes/ UpdateAssessmentStatus_NotLatestSoftRestriction, waasapitypes/ UpdateAssessmentStatus_NotLatestUnknown, waasapitypes/ UpdateAssessmentStatus_NotLatestTargetedVersion, waasapitypes/UpdateAssessmentStatus
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
req.typenames: UpdateAssessmentStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateAssessmentStatus
 - waasapitypes/tagUpdateAssessmentStatus
 - UpdateAssessmentStatus
 - waasapitypes/UpdateAssessmentStatus
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
 - UpdateAssessmentStatus
---

# UpdateAssessmentStatus enumeration


## -description

Describes how up-to-date the OS on a device is. <b>UpdateAssessmentStatus</b> is used by the <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a> and <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a> structures, in the <b>assessmentForCurrent</b>, <b>assessmentForUpToDate</b>, and <b>securityStatus</b> members. Exactly one constant is returned.

## -enum-fields

### -field UpdateAssessmentStatus_Latest:0

This result within <b>assessmentForCurrent</b> implies that the device is on the latest feature update and quality update available for that device. Within <b>assessmentForUpToDate</b>, this result implies that the device is on the latest quality update for the release of Windows it is running.

### -field UpdateAssessmentStatus_NotLatestSoftRestriction

The latest feature update has not been installed due to a soft restriction. When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX. This status only applies to <b>assessmentForCurrent</b>.

### -field UpdateAssessmentStatus_NotLatestHardRestriction

The latest feature update has not been installed due to a hard restriction. When a hard restriction has been placed on an update, the update is not applicable to the device. This status only applies to <b>assessmentForCurrent</b>.

### -field UpdateAssessmentStatus_NotLatestEndOfSupport

The device is not on the latest update because the device's feature update is no longer supported by Microsoft. When Microsoft stops supporting a feature release, this status will be returned for both <b>assessmentForCurrent</b> and <b>assessmentForUpToDate</b>. 
 


<div class="alert"><b>Note</b>   When <b>UpdateAssessmentStatus_NotLatestEndOfSupport</b> is returned, the assessment's <b>UpdateImpactLevel</b> is always <b>UpdateImpactLevel_High</b>.</div>
<div> </div>

### -field UpdateAssessmentStatus_NotLatestServicingTrain

The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update. For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned. This status only applies to <b>assessmentForCurrent</b>.

### -field UpdateAssessmentStatus_NotLatestDeferredFeature

The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy. Determining <b>daysOutOfDate</b> takes into account deferral policies; <b>daysOutOfDate</b> will not begin incrementing until the deferral period has expired. This status only applies to <b>assessmentForCurrent</b>.

### -field UpdateAssessmentStatus_NotLatestDeferredQuality

The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.  Determining <b>daysOutOfDate</b> takes into account deferral policies; <b>daysOutOfDate</b> will not begin incrementing until the deferral period has expired.

### -field UpdateAssessmentStatus_NotLatestPausedFeature

The device is not on the latest feature update due to the device having paused Feature Updates. Whether a device is paused is not factored into the calculation of <b>daysOutOfDate</b>. This status only applies to <b>assessmentForCurrent</b>.

### -field UpdateAssessmentStatus_NotLatestPausedQuality

The device is not on the latest quality update due to the device having paused Quality Updates. Whether a device is paused is not factored into the calculation of <b>daysOutOfDate</b>. <b>daysOutOfDate</b> does not factor whether a device is paused into its calculation.

### -field UpdateAssessmentStatus_NotLatestManaged

The device is not on the latest update because the approval of updates is not done through Windows Update.

### -field UpdateAssessmentStatus_NotLatestUnknown

The device is not on the latest update due to a reason that cannot be determined by the assessment.

### -field UpdateAssessmentStatus_NotLatestTargetedVersion

The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy. This policy is keeping the device on the targeted feature release version.

## -remarks

This enumeration is used most often with the <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a>  and <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a> structures, which are in turn used with the <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a> method for <a href="/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor">IWaaSAssessor</a>.
