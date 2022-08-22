---
UID: NN:oaidl.ITypeLib
title: ITypeLib (oaidl.h)
description: Represents a type library, the data that describes a set of objects. (ITypeLib)
helpviewer_keywords: ["ITypeLib","ITypeLib interface [Automation]","ITypeLib interface [Automation]","described","_oa96_ITypeLib_Interface","automat.itypelib","oaidl/ITypeLib"]
old-location: automat\itypelib.htm
tech.root: automat
ms.assetid: c1e5d71f-6a4e-45f3-811d-f57024f81a55
ms.date: 12/05/2018
ms.keywords: ITypeLib, ITypeLib interface [Automation], ITypeLib interface [Automation],described, _oa96_ITypeLib_Interface, automat.itypelib, oaidl/ITypeLib
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
 - ITypeLib
 - oaidl/ITypeLib
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
 - ITypeLib
---

# ITypeLib interface


## -description

Represents a type library, the data that describes a set of objects. A type library can be a stand-alone binary file (.TLB), a resource in a dynamic link library or executable file (.DLL, .OLB, or .EXE).

## -inheritance

The <b>ITypeLib</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeLib</b> also has these types of members:

## -remarks

The system registry contains a list of all the installed type libraries. Type library organization is illustrated in the following figure:

:::image type="content" source="./images/oa03_10.Png" border="false" alt-text="Diagram showing the organization of installed type libraries as they are listed in the system registry.":::

The <b>ITypeLib</b> interface provides methods for accessing a library of type descriptions. This interface supports the following:  

<ul>
<li>
Generalized containment for type information. <b>ITypeLib</b> allows iteration over the type descriptions contained in the library.

</li>
<li>
Global functions and data. A type library can contain descriptions of a set of modules (.DLLs) that exports data and functions. The type library supports compiling references to the exported data and functions.

</li>
<li>
General information, including a user-readable name for the library and help for the library as a whole.

</li>
</ul>

## -see-also

<a href="/previous-versions/ms221172(v=vs.85)">Type Description Interfaces and Functions </a>
