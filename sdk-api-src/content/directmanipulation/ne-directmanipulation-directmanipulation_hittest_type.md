---
UID: NE:directmanipulation.DIRECTMANIPULATION_HITTEST_TYPE
title: DIRECTMANIPULATION_HITTEST_TYPE (directmanipulation.h)
description: Defines how hit testing is handled by Direct Manipulation when using a dedicated hit-test thread registered through RegisterHitTestTarget.
helpviewer_keywords: ["DIRECTMANIPULATION_HITTEST_TYPE","DIRECTMANIPULATION_HITTEST_TYPE enumeration [Direct Manipulation]","DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS","DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS","DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS","directmanipulation.directmanipulation_hittest_type","directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE","directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS","directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS","directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS"]
old-location: directmanipulation\directmanipulation_hittest_type.htm
tech.root: directmanipulation
ms.assetid: 68e65695-9f28-4da4-9080-4030ed10c6ed
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_HITTEST_TYPE, DIRECTMANIPULATION_HITTEST_TYPE enumeration [Direct Manipulation], DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS, DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS, DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS, directmanipulation.directmanipulation_hittest_type, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS, directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS
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
req.typenames: DIRECTMANIPULATION_HITTEST_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_HITTEST_TYPE
 - directmanipulation/DIRECTMANIPULATION_HITTEST_TYPE
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
 - DIRECTMANIPULATION_HITTEST_TYPE
---

# DIRECTMANIPULATION_HITTEST_TYPE enumeration


## -description

Defines how hit testing is handled by <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> when using a dedicated hit-test thread registered through <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget">RegisterHitTestTarget</a>.

## -enum-fields

### -field DIRECTMANIPULATION_HITTEST_TYPE_ASYNCHRONOUS:0

The hit-test thread receives <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages and specifies whether to call <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a>. If <b>SetContact</b> is not called, the contact will not be associated with a viewport.

### -field DIRECTMANIPULATION_HITTEST_TYPE_SYNCHRONOUS:0x1

The UI thread always receives <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages after the hit-test thread. A call to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> is not required.

### -field DIRECTMANIPULATION_HITTEST_TYPE_AUTO_SYNCHRONOUS:0x2

The UI thread receives <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages only when <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a> isn't called by the hit-test thread.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
