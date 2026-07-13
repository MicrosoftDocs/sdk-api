---
UID: NN:oaidl.ITypeLib2
title: ITypeLib2 (oaidl.h)
description: Represents a type library, the data that describes a set of objects. (ITypeLib2)
helpviewer_keywords: ["ITypeLib2","ITypeLib2 interface [Automation]","ITypeLib2 interface [Automation]","described","_oa96_ITypeLib2_Interface","automat.itypelib2","oaidl/ITypeLib2"]
old-location: automat\itypelib2.htm
tech.root: automat
ms.assetid: 47561b53-3f7b-4939-8b86-5acb5eaeea5a
ms.date: 12/05/2018
ms.keywords: ITypeLib2, ITypeLib2 interface [Automation], ITypeLib2 interface [Automation],described, _oa96_ITypeLib2_Interface, automat.itypelib2, oaidl/ITypeLib2
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ITypeLib2
 - oaidl/ITypeLib2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeLib2
---

# ITypeLib2 interface


## -description

Represents a type library, the data that describes a set of objects.

The <b>ITypeLib2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a> interface. This allows <b>ITypeLib</b> to cast to an <b>ITypeLib2</b> in performance-sensitive cases, rather than perform extra QueryInterface and Release calls.

## -inheritance

The <b>ITypeLib2</b> interface inherits from <b>ITypeLib</b>. <b>ITypeLib2</b> also has these types of members:

## -see-also

<a href="/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>
