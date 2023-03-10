---
UID: NN:comsvcs.IObjectContext
title: IObjectContext (comsvcs.h)
description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object. (IObjectContext)
helpviewer_keywords: ["IObjectContext","IObjectContext interface [COM+]","IObjectContext interface [COM+]","described","_cos_IObjectContext","comsvcs/IObjectContext","cos.iobjectcontext"]
old-location: cos\iobjectcontext.htm
tech.root: cos
ms.assetid: 9395bc9a-dfe5-428a-839f-1c4ad090f636
ms.date: 12/05/2018
ms.keywords: IObjectContext, IObjectContext interface [COM+], IObjectContext interface [COM+],described, _cos_IObjectContext, comsvcs/IObjectContext, cos.iobjectcontext
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
 - IObjectContext
 - comsvcs/IObjectContext
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
 - IObjectContext
---

# IObjectContext interface


## -description

Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.

## -inheritance

The <b>IObjectContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContext</b> also has these types of members:

## -remarks

As with any COM object, you must release an <b>IObjectContext</b> object when you are finished using it, unless it is a local variable.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-getobjectcontext">GetObjectContext</a>
