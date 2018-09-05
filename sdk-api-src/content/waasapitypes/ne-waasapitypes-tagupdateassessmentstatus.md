---
UID: NE:waasapitypes.tagUpdateAssessmentStatus
title: tagUpdateAssessmentStatus
author: windows-sdk-content
description: Describes how up-to-date the OS on a device is.
old-location: base\updateassessmentstatus.htm
old-project: SysInfo
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UpdateAssessmentStatus, UpdateAssessmentStatus enumeration, UpdateAssessmentStatus_Latest, UpdateAssessmentStatus_NotLatestDeferredFeature, UpdateAssessmentStatus_NotLatestDeferredQuality, UpdateAssessmentStatus_NotLatestEndOfSupport, UpdateAssessmentStatus_NotLatestHardRestriction, UpdateAssessmentStatus_NotLatestManaged, UpdateAssessmentStatus_NotLatestPausedFeature, UpdateAssessmentStatus_NotLatestPausedQuality, UpdateAssessmentStatus_NotLatestServicingTrain, UpdateAssessmentStatus_NotLatestSoftRestriction, UpdateAssessmentStatus_NotLatestUnknown, base.updateassessmentstatus, tagUpdateAssessmentStatus, waasapitypes/ UpdateAssessmentStatus_Latest, waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredFeature, waasapitypes/ UpdateAssessmentStatus_NotLatestDeferredQuality, waasapitypes/ UpdateAssessmentStatus_NotLatestEndOfSupport, waasapitypes/ UpdateAssessmentStatus_NotLatestHardRestriction, waasapitypes/ UpdateAssessmentStatus_NotLatestManaged, waasapitypes/ UpdateAssessmentStatus_NotLatestPausedFeature, waasapitypes/ UpdateAssessmentStatus_NotLatestPausedQuality, waasapitypes/ UpdateAssessmentStatus_NotLatestServicingTrain, waasapitypes/ UpdateAssessmentStatus_NotLatestSoftRestriction, waasapitypes/ UpdateAssessmentStatus_NotLatestUnknown, waasapitypes/UpdateAssessmentStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: waasapitypes.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UpdateAssessmentStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - waasapitypes.h
api_name:
 - UpdateAssessmentStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# tagUpdateAssessmentStatus enumeration


## -description


Describes how up-to-date the OS on a device is.<b>UpdateAssessmentStatus</b> is used by the <a href="https://msdn.microsoft.com/BD456DF6-4A29-41B4-8EB4-8F29910981E7">UpdateAssessment</a> and <a href="https://msdn.microsoft.com/D76D0587-E31E-48D2-9DF6-33444E4CA325">OSUpdateAssessment</a> structures, in the <b>assessmentForCurrent</b>, <b>assessmentForUpToDate</b>, and <b>securityStatus</b> members. Exactly one constant is returned.


## -enum-fields




### -field UpdateAssessmentStatus_Latest

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


## -remarks



This enumeration is used most often with the <a href="https://msdn.microsoft.com/BD456DF6-4A29-41B4-8EB4-8F29910981E7">UpdateAssessment</a>  and <a href="https://msdn.microsoft.com/D76D0587-E31E-48D2-9DF6-33444E4CA325">OSUpdateAssessment</a> structures, which are in turn used with the <a href="https://msdn.microsoft.com/3123362E-6A1C-49BD-BE9C-0B8506EA944B">GetOSUpdateAssessment</a> method for <a href="https://msdn.microsoft.com/CE5D99C9-2348-4566-AC94-DFBA5B583503">IWaaSAssessor</a>.



