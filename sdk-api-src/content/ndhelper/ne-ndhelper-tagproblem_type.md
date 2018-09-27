---
UID: NE:ndhelper.tagPROBLEM_TYPE
title: tagPROBLEM_TYPE
author: windows-sdk-content
description: The PROBLEM_TYPE enumeration describes the type of problem a helper class indicates is present.
old-location: ndf\problem_type.htm
tech.root: NDF
ms.assetid: cf5a4205-b79f-4de6-b153-0955c6ff4e11
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PROBLEM_TYPE, PROBLEM_TYPE enumeration [NDF], PT_DOWN_STREAM_HEALTH, PT_HIGHER_UTILIZATION, PT_HIGH_UTILIZATION, PT_LOWER_HEALTH, PT_LOW_HEALTH, PT_UP_STREAM_UTILIZATION, ndf.problem_type, ndhelper/PROBLEM_TYPE, ndhelper/PT_DOWN_STREAM_HEALTH, ndhelper/PT_HIGHER_UTILIZATION, ndhelper/PT_HIGH_UTILIZATION, ndhelper/PT_LOWER_HEALTH, ndhelper/PT_LOW_HEALTH, ndhelper/PT_UP_STREAM_UTILIZATION, tagPROBLEM_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - PROBLEM_TYPE
product: Windows
targetos: Windows
req.typenames: PROBLEM_TYPE
req.redist: 
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

