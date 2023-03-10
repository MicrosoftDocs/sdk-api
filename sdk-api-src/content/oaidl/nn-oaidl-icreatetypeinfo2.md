---
UID: NN:oaidl.ICreateTypeInfo2
title: ICreateTypeInfo2 (oaidl.h)
description: Provides the tools for creating and administering the type information defined through the type description. (ICreateTypeInfo2)
helpviewer_keywords: ["ICreateTypeInfo2","ICreateTypeInfo2 interface [Automation]","ICreateTypeInfo2 interface [Automation]","described","_oa96_ICreateTypeInfo2_Interface","automat.icreatetypeinfo2","oaidl/ICreateTypeInfo2"]
old-location: automat\icreatetypeinfo2.htm
tech.root: automat
ms.assetid: 34dc6f52-6864-4edb-b22d-80eef05d4c8c
ms.date: 12/05/2018
ms.keywords: ICreateTypeInfo2, ICreateTypeInfo2 interface [Automation], ICreateTypeInfo2 interface [Automation],described, _oa96_ICreateTypeInfo2_Interface, automat.icreatetypeinfo2, oaidl/ICreateTypeInfo2
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
 - ICreateTypeInfo2
 - oaidl/ICreateTypeInfo2
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
 - ICreateTypeInfo2
---

# ICreateTypeInfo2 interface


## -description

Provides the tools for creating and administering the type information defined through the type description. Derives from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>, and adds methods for deleting items that have been added through ICreateTypeInfo.

The <a href="/previous-versions/windows/desktop/automat/out">ICreateTypeInfo::LayOut</a> method provides a way for the creator of the type information to check for any errors. A call to QueryInterface can be made to the ICreateTypeInfo instance at any time for its ITypeInfo interface. Calling any of the methods in the ITypeInfointerface that require layout information lays out the type information automatically.

## -inheritance

The <b>ICreateTypeInfo2</b> interface inherits from <b>ICreateTypeInfo</b>. <b>ICreateTypeInfo2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
