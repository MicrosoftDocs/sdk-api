---
UID: NF:objidl.IBindCtx.SetBindOptions
title: IBindCtx::SetBindOptions (objidl.h)
description: Sets new values for the binding parameters stored in the bind context.
helpviewer_keywords: ["IBindCtx interface [COM]","SetBindOptions method","IBindCtx.SetBindOptions","IBindCtx::SetBindOptions","SetBindOptions","SetBindOptions method [COM]","SetBindOptions method [COM]","IBindCtx interface","_com_ibindctx_setbindoptions","com.ibindctx_setbindoptions","objidl/IBindCtx::SetBindOptions"]
old-location: com\ibindctx_setbindoptions.htm
tech.root: com
ms.assetid: 9dcce48e-567e-42b4-8df2-2bc861cb5fcb
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],SetBindOptions method, IBindCtx.SetBindOptions, IBindCtx::SetBindOptions, SetBindOptions, SetBindOptions method [COM], SetBindOptions method [COM],IBindCtx interface, _com_ibindctx_setbindoptions, com.ibindctx_setbindoptions, objidl/IBindCtx::SetBindOptions
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IBindCtx::SetBindOptions
 - objidl/IBindCtx::SetBindOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IBindCtx.SetBindOptions
---

# IBindCtx::SetBindOptions


## -description

Sets new values for the binding parameters stored in the bind context.

## -parameters

### -param pbindopts [in]

A pointer to a [BIND_OPTS3](/windows/win32/api/objidl/ns-objidl-bind_opts3-r1) structure containing the binding parameters.

## -returns

This method can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

A bind context contains a block of parameters that are common to most <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> operations. These parameters do not change as the operation moves from piece to piece of a composite moniker.

Subsequent binding operations can call <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getbindoptions">IBindCtx::GetBindOptions</a> to retrieve these parameters.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method can be called by moniker clients (those who use monikers to acquire interface pointers to objects).

When you first create a bind context by using the <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function, the fields of the <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure are initialized to the following values:


``` syntax
    cbStruct = sizeof(BIND_OPTS); 
    grfFlags = 0; 
    grfMode = STGM_READWRITE; 
    dwTickCountDeadline = 0; 

```

You can use the <b>IBindCtx::SetBindOptions</b> method to modify these values before using the bind context, if you want values other than the defaults.

<b>SetBindOptions</b> copies the members of the specified structure, but not the <a href="/windows/desktop/api/objidl/ns-objidl-coserverinfo">COSERVERINFO</a> structure and the pointers it contains. Callers may not free these pointers until the bind context is released.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>



[BIND_OPTS2](/windows/win32/api/objidl/ns-objidl-bind_opts2-r1)



[BIND_OPTS3](/windows/win32/api/objidl/ns-objidl-bind_opts3-r1)



<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>
