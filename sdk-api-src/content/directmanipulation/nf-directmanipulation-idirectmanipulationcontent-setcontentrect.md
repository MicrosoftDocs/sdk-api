---
UID: NF:directmanipulation.IDirectManipulationContent.SetContentRect
title: IDirectManipulationContent::SetContentRect (directmanipulation.h)
description: Specifies the bounding rectangle of the content, relative to its viewport.
helpviewer_keywords: ["IDirectManipulationContent interface [Direct Manipulation]","SetContentRect method","IDirectManipulationContent.SetContentRect","IDirectManipulationContent::SetContentRect","SetContentRect","SetContentRect method [Direct Manipulation]","SetContentRect method [Direct Manipulation]","IDirectManipulationContent interface","directmanipulation.idirectmanipulationcontent_setcontentrect","directmanipulation/IDirectManipulationContent::SetContentRect"]
old-location: directmanipulation\idirectmanipulationcontent_setcontentrect.htm
tech.root: directmanipulation
ms.assetid: 41b14e56-ba24-4ad2-9dac-28daf7d13c6a
ms.date: 12/05/2018
ms.keywords: IDirectManipulationContent interface [Direct Manipulation],SetContentRect method, IDirectManipulationContent.SetContentRect, IDirectManipulationContent::SetContentRect, SetContentRect, SetContentRect method [Direct Manipulation], SetContentRect method [Direct Manipulation],IDirectManipulationContent interface, directmanipulation.idirectmanipulationcontent_setcontentrect, directmanipulation/IDirectManipulationContent::SetContentRect
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
 - IDirectManipulationContent::SetContentRect
 - directmanipulation/IDirectManipulationContent::SetContentRect
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
 - IDirectManipulationContent.SetContentRect
---

# IDirectManipulationContent::SetContentRect


## -description

Specifies the bounding rectangle of the content, relative to its viewport.

## -parameters

### -param contentSize [in]

The bounding rectangle of the content.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default bounding rectangle is (-<a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, -<a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>).

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>