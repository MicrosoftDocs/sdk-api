---
UID: NE:directmanipulation.DIRECTMANIPULATION_INPUT_MODE
title: DIRECTMANIPULATION_INPUT_MODE
author: windows-sdk-content
description: Defines the threading behavior for SetInputMode or SetUpdateMode. The exact meaning of each constant depends on the method called.
old-location: directmanipulation\directmanipulation_input_mode.htm
tech.root: directmanipulation
ms.assetid: 92839109-91d5-45fc-85d0-dc5a14e4ebf0
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DIRECTMANIPULATION_INPUT_MODE, DIRECTMANIPULATION_INPUT_MODE enumeration [Direct Manipulation], DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC, DIRECTMANIPULATION_INPUT_MODE_MANUAL, directmanipulation.directmanipulation_input_mode, directmanipulation/DIRECTMANIPULATION_INPUT_MODE, directmanipulation/DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC, directmanipulation/DIRECTMANIPULATION_INPUT_MODE_MANUAL
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
 - DIRECTMANIPULATION_INPUT_MODE
product: Windows
targetos: Windows
req.typenames: DIRECTMANIPULATION_INPUT_MODE
req.redist: 
---

# DIRECTMANIPULATION_INPUT_MODE enumeration


## -description


Defines the threading behavior for <a href="https://msdn.microsoft.com/2be1c8a1-a729-4851-b103-b108b9a96e2d">SetInputMode</a> or <a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a>. The exact meaning of each constant depends on the method called.


## -enum-fields




### -field DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC

Input is automatically passed to the viewport in an independent thread.


### -field DIRECTMANIPULATION_INPUT_MODE_MANUAL

Input is manually passed by   the app on its thread via the <a href="https://msdn.microsoft.com/ed7fa19b-acfe-4d5d-bd71-a77e5016fe68">ProcessInput</a> method.


## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

