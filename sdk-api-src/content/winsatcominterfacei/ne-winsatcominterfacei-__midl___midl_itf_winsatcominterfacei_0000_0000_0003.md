---
UID: NE:winsatcominterfacei.__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003
title: "__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003"
author: windows-sdk-content
description: Defines the possible subcomponents of an assessment.
old-location: winsat\winsat_assessment_type.htm
old-project: winsat
ms.assetid: 7e54df13-4415-42b8-b140-e35ea440ef68
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WINSAT_ASSESSMENT_CPU, WINSAT_ASSESSMENT_D3D, WINSAT_ASSESSMENT_DISK, WINSAT_ASSESSMENT_GRAPHICS, WINSAT_ASSESSMENT_MEMORY, WINSAT_ASSESSMENT_TYPE, WINSAT_ASSESSMENT_TYPE enumeration [WinSAT], __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003, winsat.winsat_assessment_type, winsatcominterfacei/WINSAT_ASSESSMENT_CPU, winsatcominterfacei/WINSAT_ASSESSMENT_D3D, winsatcominterfacei/WINSAT_ASSESSMENT_DISK, winsatcominterfacei/WINSAT_ASSESSMENT_GRAPHICS, winsatcominterfacei/WINSAT_ASSESSMENT_MEMORY, winsatcominterfacei/WINSAT_ASSESSMENT_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WINSAT_ASSESSMENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsatcominterfacei.h
api_name:
 - WINSAT_ASSESSMENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0003 enumeration


## -description


<p class="CCE_Message">[WINSAT_ASSESSMENT_TYPE may be altered or unavailable for releases after Windows 8.1.]

Defines the possible subcomponents of an assessment.


## -enum-fields




### -field WINSAT_ASSESSMENT_MEMORY

Assess the memory of the computer.


### -field WINSAT_ASSESSMENT_CPU

Assess the processors on the computer.


### -field WINSAT_ASSESSMENT_DISK

Assess the primary hard disk on the computer.


### -field WINSAT_ASSESSMENT_D3D

After Windows 8.1, WinSAT no longer assesses the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment. For compatibility, WinSAT reports sentinel values for the metrics and scores, however these are not calculated in real time. 


### -field WINSAT_ASSESSMENT_GRAPHICS

  Assess the video card abilities required for Desktop Window Manager (DWM) composition.


## -see-also




<a href="https://msdn.microsoft.com/dfa4d740-2dfd-41b5-a0be-a241f9ece939">IProvideWinSATResultsInfo::GetAssessmentInfo</a>
 

 

