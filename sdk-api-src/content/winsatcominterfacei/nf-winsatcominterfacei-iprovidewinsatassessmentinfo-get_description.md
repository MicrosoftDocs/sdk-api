---
UID: NF:winsatcominterfacei.IProvideWinSATAssessmentInfo.get_Description
title: IProvideWinSATAssessmentInfo::get_Description (winsatcominterfacei.h)
description: Retrieves the description of the subcomponent.
helpviewer_keywords: ["Description property [WinSAT]","Description property [WinSAT]","IProvideWinSATAssessmentInfo interface","IProvideWinSATAssessmentInfo interface [WinSAT]","Description property","IProvideWinSATAssessmentInfo.Description","IProvideWinSATAssessmentInfo.get_Description","IProvideWinSATAssessmentInfo::Description","IProvideWinSATAssessmentInfo::get_Description","get_Description","winsat.iprovidewinsatassessmentinfo_description","winsatcominterfacei/IProvideWinSATAssessmentInfo::Description","winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Description"]
old-location: winsat\iprovidewinsatassessmentinfo_description.htm
tech.root: WinSAT
ms.assetid: e598ad5e-e0b9-494a-ba87-0ae7c960deee
ms.date: 12/05/2018
ms.keywords: Description property [WinSAT], Description property [WinSAT],IProvideWinSATAssessmentInfo interface, IProvideWinSATAssessmentInfo interface [WinSAT],Description property, IProvideWinSATAssessmentInfo.Description, IProvideWinSATAssessmentInfo.get_Description, IProvideWinSATAssessmentInfo::Description, IProvideWinSATAssessmentInfo::get_Description, get_Description, winsat.iprovidewinsatassessmentinfo_description, winsatcominterfacei/IProvideWinSATAssessmentInfo::Description, winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Description
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Winsatapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProvideWinSATAssessmentInfo::get_Description
 - winsatcominterfacei/IProvideWinSATAssessmentInfo::get_Description
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IProvideWinSATAssessmentInfo.Description
 - IProvideWinSATAssessmentInfo.get_Description
---

# IProvideWinSATAssessmentInfo::get_Description


## -description

<p class="CCE_Message">[IProvideWinSATAssessmentInfo::Description may be altered or unavailable for releases after Windows 8.1.]

Retrieves the description of the subcomponent.

This property is read-only.

## -parameters

## -remarks

The description provided depends on the subcomponent. For example, the description for the CPU subcomponent identifies the processor, and the description for the memory subcomponent indicates the amount of available RAM.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo">IProvideWinSATAssessmentInfo</a>