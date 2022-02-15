---
UID: NE:winsatcominterfacei.__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003
title: WINSAT_ASSESSMENT_TYPE (winsatcominterfacei.h)
description: Defines the possible subcomponents of an assessment.
helpviewer_keywords: ["WINSAT_ASSESSMENT_CPU","WINSAT_ASSESSMENT_D3D","WINSAT_ASSESSMENT_DISK","WINSAT_ASSESSMENT_GRAPHICS","WINSAT_ASSESSMENT_MEMORY","WINSAT_ASSESSMENT_TYPE","WINSAT_ASSESSMENT_TYPE enumeration [WinSAT]","winsat.winsat_assessment_type","winsatcominterfacei/WINSAT_ASSESSMENT_CPU","winsatcominterfacei/WINSAT_ASSESSMENT_D3D","winsatcominterfacei/WINSAT_ASSESSMENT_DISK","winsatcominterfacei/WINSAT_ASSESSMENT_GRAPHICS","winsatcominterfacei/WINSAT_ASSESSMENT_MEMORY","winsatcominterfacei/WINSAT_ASSESSMENT_TYPE"]
old-location: winsat\winsat_assessment_type.htm
tech.root: WinSAT
ms.assetid: 7e54df13-4415-42b8-b140-e35ea440ef68
ms.date: 12/05/2018
ms.keywords: WINSAT_ASSESSMENT_CPU, WINSAT_ASSESSMENT_D3D, WINSAT_ASSESSMENT_DISK, WINSAT_ASSESSMENT_GRAPHICS, WINSAT_ASSESSMENT_MEMORY, WINSAT_ASSESSMENT_TYPE, WINSAT_ASSESSMENT_TYPE enumeration [WinSAT], winsat.winsat_assessment_type, winsatcominterfacei/WINSAT_ASSESSMENT_CPU, winsatcominterfacei/WINSAT_ASSESSMENT_D3D, winsatcominterfacei/WINSAT_ASSESSMENT_DISK, winsatcominterfacei/WINSAT_ASSESSMENT_GRAPHICS, winsatcominterfacei/WINSAT_ASSESSMENT_MEMORY, winsatcominterfacei/WINSAT_ASSESSMENT_TYPE
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINSAT_ASSESSMENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003
 - winsatcominterfacei/__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003
 - WINSAT_ASSESSMENT_TYPE
 - winsatcominterfacei/WINSAT_ASSESSMENT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsatcominterfacei.h
api_name:
 - WINSAT_ASSESSMENT_TYPE
---

# WINSAT_ASSESSMENT_TYPE enumeration


## -description

<p class="CCE_Message">[WINSAT_ASSESSMENT_TYPE may be altered or unavailable for releases after Windows 8.1.]

Defines the possible subcomponents of an assessment.

## -enum-fields

### -field WINSAT_ASSESSMENT_MEMORY:0

Assess the memory of the computer.

### -field WINSAT_ASSESSMENT_CPU:1

Assess the processors on the computer.

### -field WINSAT_ASSESSMENT_DISK:2

Assess the primary hard disk on the computer.

### -field WINSAT_ASSESSMENT_D3D:3

After Windows 8.1, WinSAT no longer assesses the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment. For compatibility, WinSAT reports sentinel values for the metrics and scores, however these are not calculated in real time.

### -field WINSAT_ASSESSMENT_GRAPHICS:4

  Assess the video card abilities required for Desktop Window Manager (DWM) composition.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo">IProvideWinSATResultsInfo::GetAssessmentInfo</a>
