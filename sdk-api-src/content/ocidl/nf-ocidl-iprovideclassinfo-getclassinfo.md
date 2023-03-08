---
UID: NF:ocidl.IProvideClassInfo.GetClassInfo
title: IProvideClassInfo::GetClassInfo (ocidl.h)
description: Retrieves a pointer to the ITypeInfo interface for the object's type information. The type information for an object corresponds to the object's coclass entry in a type library.
helpviewer_keywords: ["GetClassInfo","GetClassInfo method [COM]","GetClassInfo method [COM]","IProvideClassInfo interface","IProvideClassInfo interface [COM]","GetClassInfo method","IProvideClassInfo.GetClassInfo","IProvideClassInfo::GetClassInfo","_com_iprovideclassinfo_getclassinfo","com.iprovideclassinfo_getclassinfo","ocidl/IProvideClassInfo::GetClassInfo"]
old-location: com\iprovideclassinfo_getclassinfo.htm
tech.root: com
ms.assetid: 9dac095d-4657-47ea-a673-4d8a96fc29bb
ms.date: 12/05/2018
ms.keywords: GetClassInfo, GetClassInfo method [COM], GetClassInfo method [COM],IProvideClassInfo interface, IProvideClassInfo interface [COM],GetClassInfo method, IProvideClassInfo.GetClassInfo, IProvideClassInfo::GetClassInfo, _com_iprovideclassinfo_getclassinfo, com.iprovideclassinfo_getclassinfo, ocidl/IProvideClassInfo::GetClassInfo
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IProvideClassInfo::GetClassInfo
 - ocidl/IProvideClassInfo::GetClassInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IProvideClassInfo.GetClassInfo
---

# IProvideClassInfo::GetClassInfo


## -description

Retrieves a pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> interface for the object's type information. The type information for an object corresponds to the object's <a href="https://msdn.microsoft.com/">coclass</a> entry in a type library.

## -parameters

### -param ppTI [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> pointer variable that receives the interface pointer to the object's type information. The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned interface pointer if this method returns successfully.

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppTI</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> before returning. If the object loads the type information from a type library, the type library itself will call <b>AddRef</b> in creating the pointer.

Because the caller cannot specify a locale identifier (LCID) when calling this method, this method must assume the neutral language, that is, LANGID_NEUTRAL, and use this value to determine what locale-specific type information to return.

This method must be implemented; E_NOTIMPL is not an acceptable return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo">IProvideClassInfo</a>
