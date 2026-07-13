---
UID: NF:objidl.IStdMarshalInfo.GetClassForHandler
title: IStdMarshalInfo::GetClassForHandler (objidl.h)
description: The IStdMarshalInfo::GetClassForHandler method (objidl.h) retrieves the CLSID of the object handler to be used in the destination process during standard marshaling.
helpviewer_keywords: ["GetClassForHandler","GetClassForHandler method [COM]","GetClassForHandler method [COM]","IStdMarshalInfo interface","IStdMarshalInfo interface [COM]","GetClassForHandler method","IStdMarshalInfo.GetClassForHandler","IStdMarshalInfo::GetClassForHandler","_com_istdmarshalinfo_getclassforhandler","com.istdmarshalinfo_getclassforhandler","objidlbase/IStdMarshalInfo::GetClassForHandler"]
old-location: com\istdmarshalinfo_getclassforhandler.htm
tech.root: com
ms.assetid: ab68f292-851d-4908-b545-4df2931fceae
ms.date: 08/15/2022
ms.keywords: GetClassForHandler, GetClassForHandler method [COM], GetClassForHandler method [COM],IStdMarshalInfo interface, IStdMarshalInfo interface [COM],GetClassForHandler method, IStdMarshalInfo.GetClassForHandler, IStdMarshalInfo::GetClassForHandler, _com_istdmarshalinfo_getclassforhandler, com.istdmarshalinfo_getclassforhandler, objidlbase/IStdMarshalInfo::GetClassForHandler
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IStdMarshalInfo::GetClassForHandler
 - objidl/IStdMarshalInfo::GetClassForHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IStdMarshalInfo.GetClassForHandler
---

# IStdMarshalInfo::GetClassForHandler


## -description

Retrieves the CLSID of the object handler to be used in the destination process during standard marshaling.

## -parameters

### -param dwDestContext [in]

The destination context, that is, the process in which the unmarshaling will be done. Possible values are taken from the enumeration <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a>.

### -param pvDestContext [in]

This parameter must be <b>NULL</b>.

### -param pClsid [out]

A pointer to the handler's CLSID.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>IStdMarshalInfo::GetClassForHandler</b> must return your own CLSID. This enables an object to be created by a different server.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istdmarshalinfo">IStdMarshalInfo</a>
