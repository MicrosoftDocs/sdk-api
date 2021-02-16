---
UID: NS:waasapitypes.tagUpdateAssessment
title: UpdateAssessment (waasapitypes.h)
description: UpdateAssessment contains information that assesses how up-to-date an installed OS is.
helpviewer_keywords: ["UpdateAssessment","UpdateAssessment structure","base.updateassessment","waasapitypes/UpdateAssessment"]
old-location: base\updateassessment.htm
tech.root: winprog
ms.assetid: BD456DF6-4A29-41B4-8EB4-8F29910981E7
ms.date: 12/05/2018
ms.keywords: UpdateAssessment, UpdateAssessment structure, base.updateassessment, waasapitypes/UpdateAssessment
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
req.typenames: UpdateAssessment
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateAssessment
 - waasapitypes/tagUpdateAssessment
 - UpdateAssessment
 - waasapitypes/UpdateAssessment
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
 - UpdateAssessment
---

# UpdateAssessment structure


## -description

<a href="/windows/desktop/SysInfo/updateassessmentstatus">UpdateAssessment</a> contains information that assesses how up-to-date an installed OS is.

## -struct-fields

### -field status

An <a href="/windows/desktop/SysInfo/updateassessmentstatus">UpdateAssessmentStatus</a> enumeration detailing how up-to-date the device is, and for what reason.

### -field impact

An <a href="/windows/desktop/SysInfo/updateimpactlevel">    UpdateImpactLevel</a> enumeration detailing whether there is any impact on the device if it has an out-of-date OS.

### -field daysOutOfDate

Describes how much time has elapsed since the device has not installed an applicable update. <b>daysOutOfDate</b> is calculated by the current time minus the time since the next applicable update has been released, minus any deferral period. Thus, if an applicable update exists but hasn’t been applied due to deferral, this is accounted for in the calculation. <b>daysOutOfDate</b> is used to calculate the update impact level.

## -remarks

This structure is used most often with <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a>, which is in turn used with the <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a> method for <a href="/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor">IWaaSAssessor</a>.

When <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a> is called, an <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a> structure is returned. Within this structure there are two <b>UpdateAssessment</b> structures: <b>assessmentForCurrent</b> and <b>assessmentForUpToDate</b>. The <b>UpdateAssessment</b> structure summarizes the assessments to determine whether a device is current or whether it is up-to-date, respectively; this is defined with the <a href="/windows/desktop/SysInfo/updateassessmentstatus">UpdateAssessmentStatus</a> enumeration. The assessment informs how many days the device has been out-of-date with <b>daysOutofDate</b>. This date is used to determine if there is any potential impact (represented by the <b>impact</b> member in this structure) to the device.