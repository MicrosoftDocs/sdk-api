---
UID: NE:directmanipulation.DIRECTMANIPULATION_INPUT_MODE
title: DIRECTMANIPULATION_INPUT_MODE (directmanipulation.h)
description: Defines the threading behavior for SetInputMode or SetUpdateMode. The exact meaning of each constant depends on the method called.
helpviewer_keywords: ["DIRECTMANIPULATION_INPUT_MODE","DIRECTMANIPULATION_INPUT_MODE enumeration [Direct Manipulation]","DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC","DIRECTMANIPULATION_INPUT_MODE_MANUAL","directmanipulation.directmanipulation_input_mode","directmanipulation/DIRECTMANIPULATION_INPUT_MODE","directmanipulation/DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC","directmanipulation/DIRECTMANIPULATION_INPUT_MODE_MANUAL"]
old-location: directmanipulation\directmanipulation_input_mode.htm
tech.root: directmanipulation
ms.assetid: 92839109-91d5-45fc-85d0-dc5a14e4ebf0
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_INPUT_MODE, DIRECTMANIPULATION_INPUT_MODE enumeration [Direct Manipulation], DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC, DIRECTMANIPULATION_INPUT_MODE_MANUAL, directmanipulation.directmanipulation_input_mode, directmanipulation/DIRECTMANIPULATION_INPUT_MODE, directmanipulation/DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC, directmanipulation/DIRECTMANIPULATION_INPUT_MODE_MANUAL
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
targetos: Windows
req.typenames: DIRECTMANIPULATION_INPUT_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_INPUT_MODE
 - directmanipulation/DIRECTMANIPULATION_INPUT_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_INPUT_MODE
---

# DIRECTMANIPULATION_INPUT_MODE enumeration


## -description

Defines the threading behavior for <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setinputmode">SetInputMode</a> or <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setupdatemode">SetUpdateMode</a>. The exact meaning of each constant depends on the method called.

## -enum-fields

### -field DIRECTMANIPULATION_INPUT_MODE_AUTOMATIC:0

Input is automatically passed to the viewport in an independent thread.

### -field DIRECTMANIPULATION_INPUT_MODE_MANUAL:1

Input is manually passed by   the app on its thread via the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-processinput">ProcessInput</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
