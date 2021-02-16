---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapType
title: IDirectManipulationPrimaryContent::SetSnapType (directmanipulation.h)
description: Specifies the type of snap point.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetSnapType method","IDirectManipulationPrimaryContent.SetSnapType","IDirectManipulationPrimaryContent::SetSnapType","SetSnapType","SetSnapType method [Direct Manipulation]","SetSnapType method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setsnaptype","directmanipulation/IDirectManipulationPrimaryContent::SetSnapType"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnaptype.htm
tech.root: directmanipulation
ms.assetid: 0f1ad54d-8c9a-4b3c-a78b-fe02cb889ca9
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapType method, IDirectManipulationPrimaryContent.SetSnapType, IDirectManipulationPrimaryContent::SetSnapType, SetSnapType, SetSnapType method [Direct Manipulation], SetSnapType method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnaptype, directmanipulation/IDirectManipulationPrimaryContent::SetSnapType
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationPrimaryContent::SetSnapType
 - directmanipulation/IDirectManipulationPrimaryContent::SetSnapType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationPrimaryContent.SetSnapType
---

# IDirectManipulationPrimaryContent::SetSnapType


## -description

Specifies the type of snap point.

## -parameters

### -param motion [in]

One or more of the <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_motion_types">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values.

### -param type [in]

One of the <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_snappoint_type">DIRECTMANIPULATION_SNAPPOINT_TYPE</a> enumeration values.

If set to <b>DIRECTMANIPULATION_SNAPPOINT_TYPE_NONE</b>, snap points specified through <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a> or <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval">SetSnapInterval</a> are cleared.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>