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

# AE_POSITION_FLAGS enumeration


## -description


Defines constants for the <a href="https://msdn.microsoft.com/2e239114-1af7-455a-a60f-2054b05e1414">AE_CURRENT_POSITION</a> structure. These constants describe the degree of validity of the current position.


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



