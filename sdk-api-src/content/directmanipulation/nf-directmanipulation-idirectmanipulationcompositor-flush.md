---
UID: NF:directmanipulation.IDirectManipulationCompositor.Flush
title: IDirectManipulationCompositor::Flush (directmanipulation.h)
description: Commits all pending updates in the compositor to the system for rendering.
helpviewer_keywords: ["Flush","Flush method [Direct Manipulation]","Flush method [Direct Manipulation]","IDirectManipulationCompositor interface","IDirectManipulationCompositor interface [Direct Manipulation]","Flush method","IDirectManipulationCompositor.Flush","IDirectManipulationCompositor::Flush","directmanipulation.idirectmanipulationcompositor_flush","directmanipulation/IDirectManipulationCompositor::Flush"]
old-location: directmanipulation\idirectmanipulationcompositor_flush.htm
tech.root: directmanipulation
ms.assetid: E6D1BD41-6D5A-4BC0-983E-CBE79613FCF8
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Direct Manipulation], Flush method [Direct Manipulation],IDirectManipulationCompositor interface, IDirectManipulationCompositor interface [Direct Manipulation],Flush method, IDirectManipulationCompositor.Flush, IDirectManipulationCompositor::Flush, directmanipulation.idirectmanipulationcompositor_flush, directmanipulation/IDirectManipulationCompositor::Flush
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
 - IDirectManipulationCompositor::Flush
 - directmanipulation/IDirectManipulationCompositor::Flush
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
 - IDirectManipulationCompositor.Flush
---

# IDirectManipulationCompositor::Flush


## -description

Commits all pending updates in the compositor to the system for rendering.



## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method enables <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> to flush any pending changes to its visuals before a system event, such as a process suspension.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>
