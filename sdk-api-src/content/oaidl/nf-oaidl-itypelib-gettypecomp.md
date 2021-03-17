---
UID: NF:oaidl.ITypeLib.GetTypeComp
title: ITypeLib::GetTypeComp (oaidl.h)
description: Enables a client compiler to bind to the types, variables, constants, and global functions for a library.
helpviewer_keywords: ["GetTypeComp","GetTypeComp method [Automation]","GetTypeComp method [Automation]","ITypeLib interface","ITypeLib interface [Automation]","GetTypeComp method","ITypeLib.GetTypeComp","ITypeLib::GetTypeComp","_oa96_ITypeLib_GetTypeComp","automat.itypelib_gettypecomp","oaidl/ITypeLib::GetTypeComp"]
old-location: automat\itypelib_gettypecomp.htm
tech.root: automat
ms.assetid: 11c22e52-b0d5-4251-b8fa-ea3efae555e6
ms.date: 12/05/2018
ms.keywords: GetTypeComp, GetTypeComp method [Automation], GetTypeComp method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeComp method, ITypeLib.GetTypeComp, ITypeLib::GetTypeComp, _oa96_ITypeLib_GetTypeComp, automat.itypelib_gettypecomp, oaidl/ITypeLib::GetTypeComp
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
 - ITypeLib::GetTypeComp
 - oaidl/ITypeLib::GetTypeComp
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
 - ITypeLib.GetTypeComp
---

# ITypeLib::GetTypeComp


## -description

Enables a client compiler to bind to the types, variables, constants, and global functions for a library.

## -parameters

### -param ppTComp [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> instance for this <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>. A client compiler uses the methods in the <b>ITypeComp</b> interface to bind to types in <b>ITypeLib</b>, as well as to the global functions, variables, and constants defined in <b>ITypeLib</b>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bind">Bind</a> function of the returned <b>TypeComp</b> binds to global functions, variables, constants, enumerated values, and coclass members. The <b>Bind</b> function also binds the names of the TYPEKIND enumerations of TKIND_MODULE, TKIND_ENUM, and TKIND_COCLASS. These names shadow any global names defined within the type information. The members of TKIND_ENUM, TKIND_MODULE, and TKIND_COCLASS types marked as Application objects can be directly bound to from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> without specifying the name of the module.




<a href="/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bind">ITypeComp::Bind</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bindtype">ITypeComp::BindType</a> accept only unqualified names. <b>ITypeLib::GetTypeComp</b> returns a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> interface, which is then used to bind to global elements in the library. The names of some types (TKIND_ENUM, TKIND_MODULE, and TKIND_COCLASS) share the name space with variables, functions, constants, and enumerators.

If a member requires qualification to differentiate it from other items in the name space, <b>GetTypeComp</b> can be called successively for each qualifier in order to bind to the desired member. This allows programming language compilers to access members of modules, enumerations, and coclasses, even though the member can't be bound to with a qualified name.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>