---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

