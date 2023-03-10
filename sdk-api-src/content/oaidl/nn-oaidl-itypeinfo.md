---
UID: NN:oaidl.ITypeInfo
title: ITypeInfo (oaidl.h)
description: Used for reading information about objects. (ITypeInfo)
helpviewer_keywords: ["ITypeInfo","ITypeInfo interface [Automation]","ITypeInfo interface [Automation]","described","_oa96_ITypeInfo_Interface","automat.itypeinfo","oaidl/ITypeInfo"]
old-location: automat\itypeinfo.htm
tech.root: automat
ms.assetid: f3356463-3373-4279-bae1-953378aa2680
ms.date: 12/05/2018
ms.keywords: ITypeInfo, ITypeInfo interface [Automation], ITypeInfo interface [Automation],described, _oa96_ITypeInfo_Interface, automat.itypeinfo, oaidl/ITypeInfo
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
 - ITypeInfo
 - oaidl/ITypeInfo
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
 - ITypeInfo
---

# ITypeInfo interface


## -description

This section describes <b>ITypeInfo</b>, an interface typically used for reading information about objects. For example, an object browser tool can use <b>ITypeInfo</b> to extract information about the characteristics and capabilities of objects from type libraries.

## -inheritance

The <b>ITypeInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeInfo</b> also has these types of members:

## -remarks

Type information interfaces are intended to describe the parts of the application that can be called by outside clients, rather than those that might be used internally to build an application.

The <b>ITypeInfo</b> interface provides access to the following:  

<ul>
<li>
The set of function descriptions associated with the type. For interfaces, this contains the set of member functions in the interface.

</li>
<li>
The set of data member descriptions associated with the type. For structures, this contains the set of fields of the type.

</li>
<li>
The general attributes of the type, such as whether it describes a structure, an interface, and so on.

</li>
</ul>
The type description of an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface can be used to implement the interface. For more information, see the description of <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createstddispatch">CreateStdDispatch</a> in <a href="/previous-versions/windows/desktop/automat/dispatch-interfaces">Dispatch Interface and API Functions</a>. 

An instance of <b>ITypeInfo</b> provides various information about the type of an object, and is used in different ways. A compiler can use an <b>ITypeInfo</b> to compile references to members of the type. A type interface browser can use it to find information about each member of the type. An <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> implementer can use it to provide automatic delegation of <b>IDispatch</b> calls to an interface.

## -see-also

<a href="/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>
