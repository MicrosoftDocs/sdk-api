---
UID: NE:directmanipulation.DIRECTMANIPULATION_HITTEST_TYPE
title: DIRECTMANIPULATION_HITTEST_TYPE
author: windows-sdk-content
description: Defines how hit testing is handled by Direct Manipulation when using a dedicated hit-test thread registered through RegisterHitTestTarget.
old-location: directmanipulation\directmanipulation_hittest_type.htm
tech.root: directmanipulation
ms.assetid: 68e65695-9f28-4da4-9080-4030ed10c6ed
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DIRECTMANIPULATION_HITTEST_TYPE, DIRECTMANIPULATION_HITTEST_TYPE enumeration [Direct Manipulation], DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS, DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS, DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS, directmanipulation.directmanipulation_hittest_type, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS
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
 - DIRECTMANIPULATION_HITTEST_TYPE
product: Windows
targetos: Windows
req.typenames: DIRECTMANIPULATION_HITTEST_TYPE
req.redist: 
---

# DIRECTMANIPULATION_HITTEST_TYPE enumeration


## -description


Defines how hit testing is handled by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> when using a dedicated hit-test thread registered through <a href="https://msdn.microsoft.com/ba71a959-b9b9-4466-9239-f3c486f5e7b3">RegisterHitTestTarget</a>.


## -enum-fields




### -field DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS

The hit-test thread receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages and specifies whether to call <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a>. If <b>SetContact</b> is not called, the contact will not be associated with a viewport.   


### -field DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS

The UI thread always receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages after the hit-test thread. A call to <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> is not required.


### -field DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS

The UI thread receives <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8ac000">WM_POINTERDOWN</a> messages only when <a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a> isn't called by the hit-test thread.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

