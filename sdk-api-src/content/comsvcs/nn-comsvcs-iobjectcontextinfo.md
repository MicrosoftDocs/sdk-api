---
UID: NN:comsvcs.IObjectContextInfo
title: IObjectContextInfo (comsvcs.h)
description: Retrieves transaction, activity, and context information on the current context object.
helpviewer_keywords: ["IObjectContextInfo","IObjectContextInfo interface [COM+]","IObjectContextInfo interface [COM+]","described","_cos_IObjectContextInfo","comsvcs/IObjectContextInfo","cos.iobjectcontextinfo"]
old-location: cos\iobjectcontextinfo.htm
tech.root: cos
ms.assetid: 76dcc6f3-f840-4672-bba9-038c1249a306
ms.date: 12/05/2018
ms.keywords: IObjectContextInfo, IObjectContextInfo interface [COM+], IObjectContextInfo interface [COM+],described, _cos_IObjectContextInfo, comsvcs/IObjectContextInfo, cos.iobjectcontextinfo
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
 - IObjectContextInfo
 - comsvcs/IObjectContextInfo
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
 - IObjectContextInfo
---

# IObjectContextInfo interface


## -description

Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

This interface has been superseded by the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a> interface.

## -inheritance

The <b>IObjectContextInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContextInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>
