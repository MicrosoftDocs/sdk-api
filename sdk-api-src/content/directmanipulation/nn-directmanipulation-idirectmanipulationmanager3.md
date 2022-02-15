---
UID: NN:directmanipulation.IDirectManipulationManager3
title: IDirectManipulationManager3 (directmanipulation.h)
description: Extends the IDirectManipulationManager2 interface that provides access to all the Direct Manipulation features and APIs available to the client application.
helpviewer_keywords: ["IDirectManipulationManager3","IDirectManipulationManager3 interface [Direct Manipulation]","IDirectManipulationManager3 interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationmanager3","directmanipulation/IDirectManipulationManager3"]
old-location: directmanipulation\idirectmanipulationmanager3.htm
tech.root: directmanipulation
ms.assetid: 566d4a36-5623-4896-b23b-3824551850b0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationManager3, IDirectManipulationManager3 interface [Direct Manipulation], IDirectManipulationManager3 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationmanager3, directmanipulation/IDirectManipulationManager3
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDirectManipulationManager3
 - directmanipulation/IDirectManipulationManager3
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
 - IDirectManipulationManager3
---

# IDirectManipulationManager3 interface


## -description

Extends the <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager2">IDirectManipulationManager2</a> interface that provides access to all the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> features and APIs available to the client application. 

The <b>IDirectManipulationManager3</b> interface adds support for retrieving an <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdefercontactservice">IDirectManipulationDeferContactService</a> object.
<div class="alert"><b>Note</b>  To obtain an <b>IDirectManipulationManager3</b> interface pointer, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an existing <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a> interface pointer.  </div><div> </div>

## -inheritance

The <b>IDirectManipulationManager3</b> interface inherits from <b>IDirectManipulationManager2</b>. <b>IDirectManipulationManager3</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
