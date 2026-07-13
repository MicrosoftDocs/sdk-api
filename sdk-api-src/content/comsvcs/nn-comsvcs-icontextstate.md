---
UID: NN:comsvcs.IContextState
title: IContextState (comsvcs.h)
description: Controls object deactivation and transaction voting by manipulating context state flags.
helpviewer_keywords: ["IContextState","IContextState interface [COM+]","IContextState interface [COM+]","described","_cos_IContextState","comsvcs/IContextState","cos.icontextstate"]
old-location: cos\icontextstate.htm
tech.root: cos
ms.assetid: cba54ad7-c670-4efb-ad3b-aca1daabc4a3
ms.date: 12/05/2018
ms.keywords: IContextState, IContextState interface [COM+], IContextState interface [COM+],described, _cos_IContextState, comsvcs/IContextState, cos.icontextstate
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
 - IContextState
 - comsvcs/IContextState
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
 - IContextState
---

# IContextState interface


## -description

Controls object deactivation and transaction voting by manipulating context state flags. By calling the methods of this interface, you can set consistent and done flags independently of each other and get the current status of each flag. Also, the methods of this interface return errors that indicate the absence of just-in-time (JIT) activation or the absence of a transaction.

## -inheritance

The <b>IContextState</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextState</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/consistent-and-done-flags">Consistent and Done Flags</a>
