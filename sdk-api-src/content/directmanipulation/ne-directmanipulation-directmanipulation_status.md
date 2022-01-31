---
UID: NE:directmanipulation.DIRECTMANIPULATION_STATUS
title: DIRECTMANIPULATION_STATUS (directmanipulation.h)
description: Defines the possible states of Direct Manipulation.
helpviewer_keywords: ["DIRECTMANIPULATION_BUILDING","DIRECTMANIPULATION_DISABLED","DIRECTMANIPULATION_ENABLED","DIRECTMANIPULATION_INERTIA","DIRECTMANIPULATION_READY","DIRECTMANIPULATION_RUNNING","DIRECTMANIPULATION_STATUS","DIRECTMANIPULATION_STATUS enumeration [Direct Manipulation]","DIRECTMANIPULATION_SUSPENDED","directmanipulation.directmanipulation_status","directmanipulation/DIRECTMANIPULATION_BUILDING","directmanipulation/DIRECTMANIPULATION_DISABLED","directmanipulation/DIRECTMANIPULATION_ENABLED","directmanipulation/DIRECTMANIPULATION_INERTIA","directmanipulation/DIRECTMANIPULATION_READY","directmanipulation/DIRECTMANIPULATION_RUNNING","directmanipulation/DIRECTMANIPULATION_STATUS","directmanipulation/DIRECTMANIPULATION_SUSPENDED"]
old-location: directmanipulation\directmanipulation_status.htm
tech.root: directmanipulation
ms.assetid: 6120702f-56f0-489d-a3b2-5f6ecac82b5e
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_BUILDING, DIRECTMANIPULATION_DISABLED, DIRECTMANIPULATION_ENABLED, DIRECTMANIPULATION_INERTIA, DIRECTMANIPULATION_READY, DIRECTMANIPULATION_RUNNING, DIRECTMANIPULATION_STATUS, DIRECTMANIPULATION_STATUS enumeration [Direct Manipulation], DIRECTMANIPULATION_SUSPENDED, directmanipulation.directmanipulation_status, directmanipulation/DIRECTMANIPULATION_BUILDING, directmanipulation/DIRECTMANIPULATION_DISABLED, directmanipulation/DIRECTMANIPULATION_ENABLED, directmanipulation/DIRECTMANIPULATION_INERTIA, directmanipulation/DIRECTMANIPULATION_READY, directmanipulation/DIRECTMANIPULATION_RUNNING, directmanipulation/DIRECTMANIPULATION_STATUS, directmanipulation/DIRECTMANIPULATION_SUSPENDED
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
req.typenames: DIRECTMANIPULATION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_STATUS
 - directmanipulation/DIRECTMANIPULATION_STATUS
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
 - DIRECTMANIPULATION_STATUS
---

# DIRECTMANIPULATION_STATUS enumeration


## -description

Defines the possible states of <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>. The viewport can process input in any state unless otherwise noted.

## -enum-fields

### -field DIRECTMANIPULATION_BUILDING:0

The viewport is being initialized and is not yet able to process input.

### -field DIRECTMANIPULATION_ENABLED:1

The viewport was successfully enabled.

### -field DIRECTMANIPULATION_DISABLED:2

The viewport is disabled and cannot process input or callbacks. The viewport can be enabled by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-enable">Enable</a>.

### -field DIRECTMANIPULATION_RUNNING:3

The viewport is currently processing input and updating content.

### -field DIRECTMANIPULATION_INERTIA:4

The viewport is moving content due to inertia.

### -field DIRECTMANIPULATION_READY:5

The viewport has completed the previous interaction.

### -field DIRECTMANIPULATION_SUSPENDED:6

The transient state of the viewport when input has been promoted to an ancestor in the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> chain.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
