---
UID: NN:comsvcs.IObjectContextActivity
title: IObjectContextActivity (comsvcs.h)
description: Retrieves the activity identifier associated with the current object context.
helpviewer_keywords: ["IObjectContextActivity","IObjectContextActivity interface [COM+]","IObjectContextActivity interface [COM+]","described","_cos_IObjectContextActivity","comsvcs/IObjectContextActivity","cos.iobjectcontextactivity"]
old-location: cos\iobjectcontextactivity.htm
tech.root: cos
ms.assetid: b3cdd835-60fd-414c-9b60-b15c07b11f34
ms.date: 12/05/2018
ms.keywords: IObjectContextActivity, IObjectContextActivity interface [COM+], IObjectContextActivity interface [COM+],described, _cos_IObjectContextActivity, comsvcs/IObjectContextActivity, cos.iobjectcontextactivity
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
 - IObjectContextActivity
 - comsvcs/IObjectContextActivity
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
 - IObjectContextActivity
---

# IObjectContextActivity interface


## -description

Retrieves the activity identifier associated with the current object context.

## -inheritance

The <b>IObjectContextActivity</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContextActivity</b> also has these types of members:

## -remarks

You obtain a reference to an object's <b>IObjectContextActivity</b> interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the object's context, as in the following example:


``` syntax
hr = m_pIObjectContext->QueryInterface(
            IID_IObjectContextActivity, 
            (void**)&m_pIObjectContextActivity);

```


## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
