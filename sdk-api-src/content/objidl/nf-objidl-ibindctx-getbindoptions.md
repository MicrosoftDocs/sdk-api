---
UID: NF:objidl.IBindCtx.GetBindOptions
title: IBindCtx::GetBindOptions (objidl.h)
description: Retrieves the binding options stored in this bind context.
helpviewer_keywords: ["GetBindOptions","GetBindOptions method [COM]","GetBindOptions method [COM]","IBindCtx interface","IBindCtx interface [COM]","GetBindOptions method","IBindCtx.GetBindOptions","IBindCtx::GetBindOptions","_com_ibindctx_getbindoptions","com.ibindctx_getbindoptions","objidl/IBindCtx::GetBindOptions"]
old-location: com\ibindctx_getbindoptions.htm
tech.root: com
ms.assetid: ccb239ee-922f-4e66-8aca-7651c0243a2b
ms.date: 12/05/2018
ms.keywords: GetBindOptions, GetBindOptions method [COM], GetBindOptions method [COM],IBindCtx interface, IBindCtx interface [COM],GetBindOptions method, IBindCtx.GetBindOptions, IBindCtx::GetBindOptions, _com_ibindctx_getbindoptions, com.ibindctx_getbindoptions, objidl/IBindCtx::GetBindOptions
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
 - IBindCtx::GetBindOptions
 - objidl/IBindCtx::GetBindOptions
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
 - IBindCtx.GetBindOptions
---

# IBindCtx::GetBindOptions


## -description

Retrieves the binding options stored in this bind context.

## -parameters

### -param pbindopts [in, out]

A pointer to an initialized structure that receives the current binding parameters on return. See [BIND_OPTS3](/windows/win32/api/objidl/ns-objidl-bind_opts3-r1).

## -returns

This method can return the standard return values E_UNEXPECTED and S_OK.

## -remarks

A bind context contains a block of parameters that are common to most <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> operations and that do not change as the operation moves from piece to piece of a composite moniker.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You typically call this method if you are writing your own moniker class. (This requires that you implement the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface.) You call this method to retrieve the parameters specified by the moniker client.

You must initialize the structure that is filled in by this method. Before calling this method, you must initialize the <b>cbStruct</b> member to the size of the structure.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>



[BIND_OPTS2](/windows/win32/api/objidl/ns-objidl-bind_opts2-r1)



[BIND_OPTS3](/windows/win32/api/objidl/ns-objidl-bind_opts3-r1)



<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>