---
UID: NE:winsatcominterfacei.__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0002
title: WINSAT_ASSESSMENT_STATE (winsatcominterfacei.h)
description: Defines the possible states of an assessment.
helpviewer_keywords: ["WINSAT_ASSESSMENT_STATE","WINSAT_ASSESSMENT_STATE enumeration [WinSAT]","WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE","WINSAT_ASSESSMENT_STATE_INVALID","WINSAT_ASSESSMENT_STATE_MAX","WINSAT_ASSESSMENT_STATE_MIN","WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE","WINSAT_ASSESSMENT_STATE_UNKNOWN","WINSAT_ASSESSMENT_STATE_VALID","winsat.winsat_assessment_state","winsatcominterfacei/WINSAT_ASSESSMENT_STATE","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_INVALID","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_MAX","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_MIN","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_UNKNOWN","winsatcominterfacei/WINSAT_ASSESSMENT_STATE_VALID"]
old-location: winsat\winsat_assessment_state.htm
tech.root: WinSAT
ms.assetid: 8d2afd18-9764-44d2-b01d-dfefc1506c6a
ms.date: 12/05/2018
ms.keywords: WINSAT_ASSESSMENT_STATE, WINSAT_ASSESSMENT_STATE enumeration [WinSAT], WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE, WINSAT_ASSESSMENT_STATE_INVALID, WINSAT_ASSESSMENT_STATE_MAX, WINSAT_ASSESSMENT_STATE_MIN, WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE, WINSAT_ASSESSMENT_STATE_UNKNOWN, WINSAT_ASSESSMENT_STATE_VALID, winsat.winsat_assessment_state, winsatcominterfacei/WINSAT_ASSESSMENT_STATE, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_INVALID, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_MAX, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_MIN, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_UNKNOWN, winsatcominterfacei/WINSAT_ASSESSMENT_STATE_VALID
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
req.typenames: WINSAT_ASSESSMENT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0002
 - winsatcominterfacei/__MIDL___MIDL_itf_winsatcominterfacei_0000_0000_0002
 - WINSAT_ASSESSMENT_STATE
 - winsatcominterfacei/WINSAT_ASSESSMENT_STATE
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
 - WINSAT_ASSESSMENT_STATE
---

# WINSAT_ASSESSMENT_STATE enumeration


## -description

<p class="CCE_Message">[WINSAT_ASSESSMENT_STATE may be altered or unavailable for releases after Windows 8.1.]

Defines the possible states of an assessment.

## -enum-fields

### -field WINSAT_ASSESSMENT_STATE_MIN:0

The minimum enumeration value for this enumeration.

### -field WINSAT_ASSESSMENT_STATE_UNKNOWN:0

The state of the assessment is unknown.

### -field WINSAT_ASSESSMENT_STATE_VALID:1

The assessment data is valid for the current computer configuration.

### -field WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE:2

The assessment data does not match the current computer configuration. The hardware on the computer has changed since the last time a formal assessment was run.

### -field WINSAT_ASSESSMENT_STATE_NOT_AVAILABLE:3

The assessment data is not available because a formal WinSAT assessment has not been run on this computer.

### -field WINSAT_ASSESSMENT_STATE_INVALID:4

The assessment data is not valid.

### -field WINSAT_ASSESSMENT_STATE_MAX:4

The maximum enumeration value for this enumeration.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_assessmentstate">IProvideWinSATResultsInfo::get_AssessmentState</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap">IProvideWinSATVisuals::get_Bitmap</a>
