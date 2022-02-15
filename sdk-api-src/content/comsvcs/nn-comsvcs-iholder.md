---
UID: NN:comsvcs.IHolder
title: IHolder (comsvcs.h)
description: Allocates or frees resources for an installed Resource Dispenser.
helpviewer_keywords: ["IHolder","IHolder interface [COM+]","IHolder interface [COM+]","described","_dtc_IHolder_Interface","comsvcs/IHolder","cos.iholder"]
old-location: cos\iholder.htm
tech.root: cos
ms.assetid: 3c852e72-2fdc-4fd0-b523-f5601154da2a
ms.date: 12/05/2018
ms.keywords: IHolder, IHolder interface [COM+], IHolder interface [COM+],described, _dtc_IHolder_Interface, comsvcs/IHolder, cos.iholder
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IHolder
 - comsvcs/IHolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IHolder
---

# IHolder interface


## -description

Allocates or frees resources for an installed Resource Dispenser. The Dispenser Manager exposes a different <b>IHolder</b> interface to each installed Resource Dispenser.

## -inheritance

The <b>IHolder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHolder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>
