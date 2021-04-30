---
UID: NF:directmanipulation.IDirectManipulationCompositor.RemoveContent
title: IDirectManipulationCompositor::RemoveContent (directmanipulation.h)
description: Removes content from the compositor.
helpviewer_keywords: ["IDirectManipulationCompositor interface [Direct Manipulation]","RemoveContent method","IDirectManipulationCompositor.RemoveContent","IDirectManipulationCompositor::RemoveContent","RemoveContent","RemoveContent method [Direct Manipulation]","RemoveContent method [Direct Manipulation]","IDirectManipulationCompositor interface","directmanipulation.idirectmanipulationcompositor_removecontent","directmanipulation/IDirectManipulationCompositor::RemoveContent"]
old-location: directmanipulation\idirectmanipulationcompositor_removecontent.htm
tech.root: directmanipulation
ms.assetid: 9bfb7fe4-abf9-4bb7-8d3f-673508053573
ms.date: 12/05/2018
ms.keywords: IDirectManipulationCompositor interface [Direct Manipulation],RemoveContent method, IDirectManipulationCompositor.RemoveContent, IDirectManipulationCompositor::RemoveContent, RemoveContent, RemoveContent method [Direct Manipulation], RemoveContent method [Direct Manipulation],IDirectManipulationCompositor interface, directmanipulation.idirectmanipulationcompositor_removecontent, directmanipulation/IDirectManipulationCompositor::RemoveContent
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
 - IDirectManipulationCompositor::RemoveContent
 - directmanipulation/IDirectManipulationCompositor::RemoveContent
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
 - IDirectManipulationCompositor.RemoveContent
---

# IDirectManipulationCompositor::RemoveContent


## -description

Removes content from the compositor.

## -parameters

### -param content [in]

The content to remove from the composition tree.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method removes content added with <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor-addcontent">AddContent</a> and restores the original relationships between parent visuals and child visuals in the composition tree. In other words, <b>RemoveContent</b> undoes <b>AddContent</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>