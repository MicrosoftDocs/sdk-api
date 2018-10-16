---
UID: NS:waasapitypes.tagUpdateAssessment
title: tagUpdateAssessment
author: windows-sdk-content
description: UpdateAssessment contains information that assesses how up-to-date an installed OS is.
old-location: base\updateassessment.htm
tech.root: sysinfo
ms.assetid: BD456DF6-4A29-41B4-8EB4-8F29910981E7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: UpdateAssessment, UpdateAssessment structure, base.updateassessment, tagUpdateAssessment, waasapitypes/UpdateAssessment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - waasapitypes.h
api_name:
 - UpdateAssessment
product: Windows
targetos: Windows
req.typenames: UpdateAssessment
req.redist: 
---

# tagUpdateAssessment structure


## -description



<a href="https://msdn.microsoft.com/157E241E-E8D8-41F8-9565-5C9298DCD1BE">UpdateAssessment</a> contains information that assesses how up-to-date an installed OS is.


## -struct-fields




### -field status

An <a href="https://msdn.microsoft.com/157E241E-E8D8-41F8-9565-5C9298DCD1BE">UpdateAssessmentStatus</a> enumeration detailing how up-to-date the device is, and for what reason. 


### -field impact

An <a href="https://msdn.microsoft.com/C7F30B63-66B0-4F37-A05B-7D366A12B640">    UpdateImpactLevel</a> enumeration detailing whether there is any impact on the device if it has an out-of-date OS.


### -field daysOutOfDate

Describes how much time has elapsed since the device has not installed an applicable update. <b>daysOutOfDate</b> is calculated by the current time minus the time since the next applicable update has been released, minus any deferral period. Thus, if an applicable update exists but hasn’t been applied due to deferral, this is accounted for in the calculation. <b>daysOutOfDate</b> is used to calculate the update impact level.


## -remarks



This structure is used most often with <a href="https://msdn.microsoft.com/D76D0587-E31E-48D2-9DF6-33444E4CA325">OSUpdateAssessment</a>, which is in turn used with the <a href="https://msdn.microsoft.com/3123362E-6A1C-49BD-BE9C-0B8506EA944B">GetOSUpdateAssessment</a> method for <a href="https://msdn.microsoft.com/CE5D99C9-2348-4566-AC94-DFBA5B583503">IWaaSAssessor</a>.

When <a href="https://msdn.microsoft.com/3123362E-6A1C-49BD-BE9C-0B8506EA944B">GetOSUpdateAssessment</a> is called, an <a href="https://msdn.microsoft.com/D76D0587-E31E-48D2-9DF6-33444E4CA325">OSUpdateAssessment</a> structure is returned. Within this structure there are two <b>UpdateAssessment</b> structures: <b>assessmentForCurrent</b> and <b>assessmentForUpToDate</b>. The <b>UpdateAssessment</b> structure summarizes the assessments to determine whether a device is current or whether it is up-to-date, respectively; this is defined with the <a href="https://msdn.microsoft.com/157E241E-E8D8-41F8-9565-5C9298DCD1BE">UpdateAssessmentStatus</a> enumeration. The assessment informs how many days the device has been out-of-date with <b>daysOutofDate</b>. This date is used to determine if there is any potential impact (represented by the <b>impact</b> member in this structure) to the device.



