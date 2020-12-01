---
UID: NE:audioengineendpoint.AE_POSITION_FLAGS
title: AE_POSITION_FLAGS (audioengineendpoint.h)
description: Defines constants for the AE_CURRENT_POSITION structure. These constants describe the degree of validity of the current position.
helpviewer_keywords: ["AE_POSITION_FLAGS","AE_POSITION_FLAGS enumeration [Remote Desktop Services]","POSITION_CONTINUOUS","POSITION_DISCONTINUOUS","POSITION_INVALID","POSITION_QPC_ERROR","audioengineendpoint/AE_POSITION_FLAGS","audioengineendpoint/POSITION_CONTINUOUS","audioengineendpoint/POSITION_DISCONTINUOUS","audioengineendpoint/POSITION_INVALID","audioengineendpoint/POSITION_QPC_ERROR","termserv.ae_position_flags"]
old-location: termserv\ae_position_flags.htm
tech.root: TermServ
ms.assetid: 09edc9ae-923c-4f57-9479-c0331588dd92
ms.date: 12/05/2018
ms.keywords: AE_POSITION_FLAGS, AE_POSITION_FLAGS enumeration [Remote Desktop Services], POSITION_CONTINUOUS, POSITION_DISCONTINUOUS, POSITION_INVALID, POSITION_QPC_ERROR, audioengineendpoint/AE_POSITION_FLAGS, audioengineendpoint/POSITION_CONTINUOUS, audioengineendpoint/POSITION_DISCONTINUOUS, audioengineendpoint/POSITION_INVALID, audioengineendpoint/POSITION_QPC_ERROR, termserv.ae_position_flags
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: AE_POSITION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AE_POSITION_FLAGS
 - audioengineendpoint/AE_POSITION_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioengineendpoint.h
api_name:
 - AE_POSITION_FLAGS
---

# AE_POSITION_FLAGS enumeration


## -description

Defines constants for the <a href="/windows/desktop/api/audioengineendpoint/ns-audioengineendpoint-ae_current_position">AE_CURRENT_POSITION</a> structure. These constants describe the degree of validity of the current position.

## -enum-fields

### -field POSITION_INVALID

The position is not valid and must not be used.

### -field POSITION_DISCONTINUOUS

The position is valid; however, there has been
    a disruption such as a glitch or state transition.
    This current position is not correlated with the previous position. The start of a stream should not reflect a discontinuity.

### -field POSITION_CONTINUOUS

The position is valid. The previous packet and the current packet are both synchronized with the timeline.

### -field POSITION_QPC_ERROR

The quality performance counter (QPC) timer value associated with this position is not accurate. This flag is set when a position error is encountered and the implementation is unable to compute an accurate QPC value that correlates with the position.

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.