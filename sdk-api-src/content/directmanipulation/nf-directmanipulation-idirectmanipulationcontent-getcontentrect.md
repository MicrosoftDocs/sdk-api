---
UID: NF:directmanipulation.IDirectManipulationContent.GetContentRect
title: IDirectManipulationContent::GetContentRect (directmanipulation.h)
description: Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).
helpviewer_keywords: ["GetContentRect","GetContentRect method [Direct Manipulation]","GetContentRect method [Direct Manipulation]","IDirectManipulationContent interface","IDirectManipulationContent interface [Direct Manipulation]","GetContentRect method","IDirectManipulationContent.GetContentRect","IDirectManipulationContent::GetContentRect","directmanipulation.idirectmanipulationcontent_getcontentrect","directmanipulation/IDirectManipulationContent::GetContentRect"]
old-location: directmanipulation\idirectmanipulationcontent_getcontentrect.htm
tech.root: directmanipulation
ms.assetid: 26a5736e-633e-4451-a339-c5f88913bcf6
ms.date: 12/05/2018
ms.keywords: GetContentRect, GetContentRect method [Direct Manipulation], GetContentRect method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetContentRect method, IDirectManipulationContent.GetContentRect, IDirectManipulationContent::GetContentRect, directmanipulation.idirectmanipulationcontent_getcontentrect, directmanipulation/IDirectManipulationContent::GetContentRect
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
 - IDirectManipulationContent::GetContentRect
 - directmanipulation/IDirectManipulationContent::GetContentRect
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
 - IDirectManipulationContent.GetContentRect
---

# IDirectManipulationContent::GetContentRect


## -description

Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).

## -parameters

### -param contentSize [out]

The bounding rectangle of the content.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the bounding rectangle  has not been set using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect">SetContentRect</a>, then <a href="/windows/desktop/UIAnimation/uianimation-error-codes">UI_E_VALUE_NOT_SET</a> is returned. However, the actual content rectangle is (-<a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, -<a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>).

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>