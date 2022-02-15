---
UID: NN:docobj.IContinueCallback
title: IContinueCallback (docobj.h)
description: Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.
helpviewer_keywords: ["IContinueCallback","IContinueCallback interface [COM]","IContinueCallback interface [COM]","described","_com_icontinuecallback","com.icontinuecallback","docobj/IContinueCallback"]
old-location: com\icontinuecallback.htm
tech.root: com
ms.assetid: 55c960be-48e3-42e1-b459-49227be62171
ms.date: 12/05/2018
ms.keywords: IContinueCallback, IContinueCallback interface [COM], IContinueCallback interface [COM],described, _com_icontinuecallback, com.icontinuecallback, docobj/IContinueCallback
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
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
 - IContinueCallback
 - docobj/IContinueCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IContinueCallback
---

# IContinueCallback interface


## -description

Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.

The <a href="/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinue">FContinue</a> method is a generic continuation request. <a href="/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinueprinting">FContinuePrinting</a> carries extra information pertaining to a printing process and is used in the context of <a href="/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>.

## -inheritance

The <b>IContinueCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContinueCallback</b> also has these types of members:

