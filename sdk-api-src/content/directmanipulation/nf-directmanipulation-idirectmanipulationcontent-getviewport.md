---
UID: NF:directmanipulation.IDirectManipulationContent.GetViewport
title: IDirectManipulationContent::GetViewport (directmanipulation.h)
description: Retrieves the viewport that contains the content.
helpviewer_keywords: ["GetViewport","GetViewport method [Direct Manipulation]","GetViewport method [Direct Manipulation]","IDirectManipulationContent interface","IDirectManipulationContent interface [Direct Manipulation]","GetViewport method","IDirectManipulationContent.GetViewport","IDirectManipulationContent::GetViewport","directmanipulation.idirectmanipulationcontent_getviewport","directmanipulation/IDirectManipulationContent::GetViewport"]
old-location: directmanipulation\idirectmanipulationcontent_getviewport.htm
tech.root: directmanipulation
ms.assetid: b03545d2-73a4-4638-818a-34f5957408e4
ms.date: 12/05/2018
ms.keywords: GetViewport, GetViewport method [Direct Manipulation], GetViewport method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetViewport method, IDirectManipulationContent.GetViewport, IDirectManipulationContent::GetViewport, directmanipulation.idirectmanipulationcontent_getviewport, directmanipulation/IDirectManipulationContent::GetViewport
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
 - IDirectManipulationContent::GetViewport
 - directmanipulation/IDirectManipulationContent::GetViewport
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
 - IDirectManipulationContent.GetViewport
---

# IDirectManipulationContent::GetViewport


## -description

Retrieves the viewport that contains the content.

## -parameters

### -param riid [in]

A reference to the identifier of the interface to use.

### -param object [out, retval]

The viewport object.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>