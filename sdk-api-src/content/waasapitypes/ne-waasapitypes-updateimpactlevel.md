---
UID: NE:waasapitypes.tagUpdateImpactLevel
title: UpdateImpactLevel (waasapitypes.h)
description: Indicates a high, medium, or low impact of a device running an out-of-date OS.
helpviewer_keywords: ["UpdateImpactLevel","UpdateImpactLevel enumeration","UpdateImpactLevel_High","UpdateImpactLevel_Low","UpdateImpactLevel_Medium","UpdateImpactLevel_None","base.updateimpactlevel","waasapitypes/ UpdateImpactLevel_Medium","waasapitypes/ UpdateImpactLevel_None","waasapitypes/UpdateImpactLevel","waasapitypes/UpdateImpactLevel_High","waasapitypes/UpdateImpactLevel_Low"]
old-location: base\updateimpactlevel.htm
tech.root: winprog
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
ms.date: 12/05/2018
ms.keywords: UpdateImpactLevel, UpdateImpactLevel enumeration, UpdateImpactLevel_High, UpdateImpactLevel_Low, UpdateImpactLevel_Medium, UpdateImpactLevel_None, base.updateimpactlevel, waasapitypes/ UpdateImpactLevel_Medium, waasapitypes/ UpdateImpactLevel_None, waasapitypes/UpdateImpactLevel, waasapitypes/UpdateImpactLevel_High, waasapitypes/UpdateImpactLevel_Low
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
req.typenames: UpdateImpactLevel
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateImpactLevel
 - waasapitypes/tagUpdateImpactLevel
 - UpdateImpactLevel
 - waasapitypes/UpdateImpactLevel
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
 - UpdateImpactLevel
---

# UpdateImpactLevel enumeration


## -description

Indicates a high, medium, or low impact of a device running an out-of-date OS. This enumeration is generally used by <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a> structures, which is in turn nested inside the returned <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a> from <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a>.

## -enum-fields

### -field UpdateImpactLevel_None:0

There is no foreseeable impact to your device. This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the <b>daysOutOfDate</b> threshold to reach a higher impact level.

### -field UpdateImpactLevel_Low

The device is not running the latest OS, but has a recent update.

### -field UpdateImpactLevel_Medium

The device is running the latest OS, but has a moderately recent update.

### -field UpdateImpactLevel_High

The device has been out-of-date for a long time. This device may have security vulnerabilities and may be missing important fixes that make Windows run better. When a device is running a version of Windows that is no longer supported, <b>UpdateImpactLevel_High</b> is always returned.

## -remarks

When <a href="/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment">GetOSUpdateAssessment</a> is called, an <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-osupdateassessment">OSUpdateAssessment</a> structure is returned. Within the structure there is an <b>assessmentForCurrent</b> and <b>assessmentForUpToDate</b>. Both of these are <a href="/windows/desktop/api/waasapitypes/ns-waasapitypes-updateassessment">UpdateAssessment</a> structures. Both members have an <b>UpdateImpactLevel</b> enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS. The These levels are determined by the value of <b>daysOutOfDate</b>.
