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

# __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0002 enumeration


## -description


<p class="CCE_Message">[WINSAT_ASSESSMENT_STATE may be altered or unavailable for releases after Windows 8.1.]

Defines the possible states of an assessment.


## -enum-fields




### -field WINSAT_ASSESSMENT_STATE_MIN

The minimum enumeration value for this enumeration.


### -field WINSAT_ASSESSMENT_STATE_UNKNOWN

The state of the assessment is unknown.


### -field WINSAT_ASSESSMENT_STATE_VALID

The assessment data is valid for the current computer configuration.


### -field WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE

The assessment data does not match the current computer configuration. The hardware on the computer has changed since the last time a formal assessment was run.


### -field WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE

The assessment data is not available because a formal WinSAT assessment has not been run on this computer.


### -field WINSAT_ASSESSMENT_STATE_INVALID

The assessment data is not valid.


### -field WINSAT_ASSESSMENT_STATE_MAX

The maximum enumeration value for this enumeration.


## -see-also




<a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::get_AssessmentState</a>



<a href="https://msdn.microsoft.com/90188fb1-3125-459e-a475-5042c2ee0a5c">IProvideWinSATVisuals::get_Bitmap</a>
 

 

