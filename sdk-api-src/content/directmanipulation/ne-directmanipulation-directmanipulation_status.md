---
UID: NE:directmanipulation.DIRECTMANIPULATION_STATUS
title: DIRECTMANIPULATION_STATUS
author: windows-sdk-content
description: Defines the possible states of Direct Manipulation.
old-location: directmanipulation\directmanipulation_status.htm
tech.root: directmanipulation
ms.assetid: 6120702f-56f0-489d-a3b2-5f6ecac82b5e
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DIRECTMANIPULATION_BUILDING, DIRECTMANIPULATION_DISABLED, DIRECTMANIPULATION_ENABLED, DIRECTMANIPULATION_INERTIA, DIRECTMANIPULATION_READY, DIRECTMANIPULATION_RUNNING, DIRECTMANIPULATION_STATUS, DIRECTMANIPULATION_STATUS enumeration [Direct Manipulation], DIRECTMANIPULATION_SUSPENDED, directmanipulation.directmanipulation_status, directmanipulation/DIRECTMANIPULATION_BUILDING, directmanipulation/DIRECTMANIPULATION_DISABLED, directmanipulation/DIRECTMANIPULATION_ENABLED, directmanipulation/DIRECTMANIPULATION_INERTIA, directmanipulation/DIRECTMANIPULATION_READY, directmanipulation/DIRECTMANIPULATION_RUNNING, directmanipulation/DIRECTMANIPULATION_STATUS, directmanipulation/DIRECTMANIPULATION_SUSPENDED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_STATUS
product: Windows
targetos: Windows
req.typenames: DIRECTMANIPULATION_STATUS
req.redist: 
---

# DIRECTMANIPULATION_STATUS enumeration


## -description


Defines the possible states of <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. The viewport can process input in any state unless otherwise noted.


## -enum-fields




### -field DIRECTMANIPULATION_BUILDING

The viewport is being initialized and is not yet able to process input.


### -field DIRECTMANIPULATION_ENABLED

The viewport was successfully enabled.


### -field DIRECTMANIPULATION_DISABLED

The viewport is disabled and cannot process input or callbacks. The viewport can be enabled by calling <a href="https://msdn.microsoft.com/47ebb502-26c6-4bff-8baf-bd825fc06755">Enable</a>.


### -field DIRECTMANIPULATION_RUNNING

The viewport is currently processing input and updating content.


### -field DIRECTMANIPULATION_INERTIA

The viewport is moving content due to inertia.


### -field DIRECTMANIPULATION_READY

The viewport has completed the previous interaction. 


### -field DIRECTMANIPULATION_SUSPENDED

The transient state of the viewport when input has been promoted to an ancestor in the <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> chain.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

