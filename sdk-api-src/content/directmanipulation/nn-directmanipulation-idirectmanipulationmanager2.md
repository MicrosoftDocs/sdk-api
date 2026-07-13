---
UID: NN:directmanipulation.IDirectManipulationManager2
title: IDirectManipulationManager2 (directmanipulation.h)
description: Extends the IDirectManipulationManager interface that provides access to all the Direct Manipulation features and APIs available to the client application.
helpviewer_keywords: ["IDirectManipulationManager2","IDirectManipulationManager2 interface [Direct Manipulation]","IDirectManipulationManager2 interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationmanager2","directmanipulation/IDirectManipulationManager2"]
old-location: directmanipulation\idirectmanipulationmanager2.htm
tech.root: directmanipulation
ms.assetid: 094C6C7D-F973-45AC-9B83-43DB9D46AF23
ms.date: 12/05/2018
ms.keywords: IDirectManipulationManager2, IDirectManipulationManager2 interface [Direct Manipulation], IDirectManipulationManager2 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager2, directmanipulation/IDirectManipulationManager2
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDirectManipulationManager2
 - directmanipulation/IDirectManipulationManager2
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
 - IDirectManipulationManager2
---

# IDirectManipulationManager2 interface


## -description

Extends the <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a> interface that provides access to all the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> features and APIs available to the client application. 

The <b>IDirectManipulationManager2</b> interface adds support for configuration behaviors that can be attached to a viewport.
<div class="alert"><b>Note</b>  To obtain an <b>IDirectManipulationManager2</b> interface pointer, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an existing <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a> interface pointer.  </div><div> </div>

## -inheritance

The <b>IDirectManipulationManager2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationManager2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
