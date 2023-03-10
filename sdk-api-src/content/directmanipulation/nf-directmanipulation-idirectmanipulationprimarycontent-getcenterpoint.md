---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.GetCenterPoint
title: IDirectManipulationPrimaryContent::GetCenterPoint (directmanipulation.h)
description: Retrieves the center point of the manipulation in content coordinates.
helpviewer_keywords: ["GetCenterPoint","GetCenterPoint method [Direct Manipulation]","GetCenterPoint method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","IDirectManipulationPrimaryContent interface [Direct Manipulation]","GetCenterPoint method","IDirectManipulationPrimaryContent.GetCenterPoint","IDirectManipulationPrimaryContent::GetCenterPoint","directmanipulation.idirectmanipulationprimarycontent_getcenterpoint","directmanipulation/IDirectManipulationPrimaryContent::GetCenterPoint"]
old-location: directmanipulation\idirectmanipulationprimarycontent_getcenterpoint.htm
tech.root: directmanipulation
ms.assetid: e38c1445-af4b-463b-8796-d72d69cb19c6
ms.date: 12/05/2018
ms.keywords: GetCenterPoint, GetCenterPoint method [Direct Manipulation], GetCenterPoint method [Direct Manipulation],IDirectManipulationPrimaryContent interface, IDirectManipulationPrimaryContent interface [Direct Manipulation],GetCenterPoint method, IDirectManipulationPrimaryContent.GetCenterPoint, IDirectManipulationPrimaryContent::GetCenterPoint, directmanipulation.idirectmanipulationprimarycontent_getcenterpoint, directmanipulation/IDirectManipulationPrimaryContent::GetCenterPoint
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
 - IDirectManipulationPrimaryContent::GetCenterPoint
 - directmanipulation/IDirectManipulationPrimaryContent::GetCenterPoint
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
 - IDirectManipulationPrimaryContent.GetCenterPoint
---

# IDirectManipulationPrimaryContent::GetCenterPoint


## -description

    Retrieves the center point of the manipulation in content coordinates. If there is no manipulation in progress, retrieves the center point of the viewport.

## -parameters

### -param centerX [out]

The center on the horizontal axis.

### -param centerY [out]

The center on the vertical axis.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>