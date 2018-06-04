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

# tagPROBLEM_TYPE enumeration


## -description


The <b>PROBLEM_TYPE</b> enumeration describes the type of problem a helper class indicates is present.


## -enum-fields




### -field PT_INVALID


### -field PT_LOW_HEALTH

A low-health problem exists within the component itself. No problems were found within local components on which this component depends. 


### -field PT_LOWER_HEALTH

A low-health problem exists within local components on which this component depends.


### -field PT_DOWN_STREAM_HEALTH

The low-health problem is in the out-of-box components this component depends on.


### -field PT_HIGH_UTILIZATION

The component's resource is being highly utilized. No high utilization was found within local components on which this component depends.


### -field PT_HIGHER_UTILIZATION

                                                       The causes of the component's high-utilization problem are from local components that depend on it.


### -field PT_UP_STREAM_UTILIZATION

The causes of the component's high-utilization problem are from upstream network components that depend on it.

