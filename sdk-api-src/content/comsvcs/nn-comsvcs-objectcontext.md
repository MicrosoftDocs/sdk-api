---
UID: NN:comsvcs.ObjectContext
title: ObjectContext (comsvcs.h)
description: Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object. (ObjectContext)
helpviewer_keywords: ["ObjectContext","ObjectContext interface [COM+]","ObjectContext interface [COM+]","described","_cos_ObjectContext","comsvcs/ObjectContext","cos.objectcontext"]
old-location: cos\objectcontext.htm
tech.root: cos
ms.assetid: 09a17e57-7224-43bc-93c7-16ab95ca2517
ms.date: 12/05/2018
ms.keywords: ObjectContext, ObjectContext interface [COM+], ObjectContext interface [COM+],described, _cos_ObjectContext, comsvcs/ObjectContext, cos.objectcontext
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
 - ObjectContext
 - comsvcs/ObjectContext
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
 - ObjectContext
---

# ObjectContext interface


## -description

Provides access to the current object's context. An object's context is primarily used when working with transactions or dealing with the security of an object.

<b>ObjectContext</b> and <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> provide the same functionality, but unlike <b>IObjectContext</b>, <b>ObjectContext</b> is compatible with Automation.

## -inheritance

The <b>ObjectContext</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ObjectContext</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
