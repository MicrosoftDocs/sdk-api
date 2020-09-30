---
UID: NF:oaidl.ITypeComp.Bind
title: ITypeComp::Bind (oaidl.h)
description: Maps a name to a member of a type, or binds global variables and functions contained in a type library.
helpviewer_keywords: ["Bind","Bind method [Automation]","Bind method [Automation]","ITypeComp interface","ITypeComp interface [Automation]","Bind method","ITypeComp.Bind","ITypeComp::Bind","_oa96_ITypeComp_Bind","automat.itypecomp_bind","oaidl/ITypeComp::Bind"]
old-location: automat\itypecomp_bind.htm
tech.root: automat
ms.assetid: 04814179-2555-4ba5-a08c-bff776c03ca3
ms.date: 12/05/2018
ms.keywords: Bind, Bind method [Automation], Bind method [Automation],ITypeComp interface, ITypeComp interface [Automation],Bind method, ITypeComp.Bind, ITypeComp::Bind, _oa96_ITypeComp_Bind, automat.itypecomp_bind, oaidl/ITypeComp::Bind
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
 - ITypeComp::Bind
 - oaidl/ITypeComp::Bind
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
 - ITypeComp.Bind
---

# ITypeComp::Bind


## -description

Maps a name to a member of a type, or binds global variables and functions contained in a type library.

## -parameters

### -param szName [in]

The name to be bound.

### -param lHashVal [in]

The hash value for the name computed by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-lhashvalofnamesys">LHashValOfNameSys</a>.

### -param wFlags [in]

One or more of the flags defined in the INVOKEKIND enumeration. Specifies whether the name was referenced as a method or a property. When binding to a variable, specify the flag INVOKE_PROPERTYGET. Specify zero to bind to any type of member.

### -param ppTInfo [out]

If a FUNCDESC or VARDESC was returned, then <i>ppTInfo</i> points to a pointer to the type description that contains the item to which it is bound.

### -param pDescKind [out]

Indicates whether the name bound to is a VARDESC, FUNCDESC, or TYPECOMP. If there was no match, DESCKIND_NONE.

### -param pBindPtr [out]

The bound-to VARDESC, FUNCDESC, or <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> interface.

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

Use <b>Bind</b> for binding to the variables and methods of a type, or for binding to the global variables and methods in a type library. The returned DESCKIND pointer <i>pDescKind</i> indicates whether the name was bound to a VARDESC, a FUNCDESC, or to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> instance. The returned <i>pBindPtr</i> points to the VARDESC, FUNCDESC, or <b>ITypeComp</b>.

If a data member or method is bound to, then ppTInfopoints to the type description that contains the method or data member.



If <b>Bind</b> binds the name to a nested binding context, it returns a pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> instance in <i>pBindPtr</i> and a null type description pointer in <i>ppTInfo</i>. For example, if the name of a type description is passed for a module (TKIND_MODULE), enumeration (TKIND_ENUM), or coclass (TKIND_COCLASS), Bind returns the <b>ITypeComp</b> instance of the type description for the module, enumeration, or coclass. This feature supports languages such as Visual Basic that allow references to members of a type description to be qualified by the name of the type description. For example, a function in a module can be referenced by <i>modulename</i>.<i>functionname.</i>

The members of TKIND_ENUM, TKIND_MODULE, and TKIND_COCLASS types marked as Application objects can be bound to directly from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a>, without specifying the name of the module. The <b>ITypeComp</b> of a coclass defers to the <b>ITypeComp</b> of its default interface.



As with other methods of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>, and <b>ITypeInfo</b>, the calling code is responsible for releasing the returned object instances or structures. If a VARDESC or FUNCDESC is returned, the caller is responsible for deleting it with the returned type description and releasing the type description instance itself. Otherwise, if an <b>ITypeComp</b> instance is returned, the caller must release it.



Special rules apply if you call a type library's <b>Bind</b> method, passing it the name of a member of an Application object class (a class that has the TYPEFLAG_FAPPOBJECT flag set). In this case, Bind returns DESCKIND_IMPLICITAPPOBJ in <i>pDescKind</i>, a VARDESC that describes the Application object in <i>pBindPtr</i>, and the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> of the Application object class in <i>ppTInfo</i>. To bind to the object, <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-gettypecomp">ITypeInfo::GetTypeComp</a> must make a call to get the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a> of the Application object class, and then reinvoke its <b>Bind</b> method with the name initially passed to the type library's <b>ITypeComp</b>.



The caller should use the returned <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> pointer (<i>ppTInfo</i>) to get the address of the member.



<div class="alert"><b>Note</b>  The <i>wflags</i> parameter is the same as the <i>wflags</i> parameter in <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>.
</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypecomp">ITypeComp</a>