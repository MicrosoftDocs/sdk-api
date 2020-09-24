---
UID: NS:callobj.__MIDL_ICallFrame_0004
title: CALLFRAME_MARSHALCONTEXT (callobj.h)
description: Provides information about the context in which marshalling should be carried out.
helpviewer_keywords: ["CALLFRAME_MARSHALCONTEXT","CALLFRAME_MARSHALCONTEXT structure [COM]","callobj/CALLFRAME_MARSHALCONTEXT","com.callframe_marshalcontext"]
old-location: com\callframe_marshalcontext.htm
tech.root: com
ms.assetid: 4ecc4646-db3f-4d0e-9c45-b78a288156e1
ms.date: 12/05/2018
ms.keywords: CALLFRAME_MARSHALCONTEXT, CALLFRAME_MARSHALCONTEXT structure [COM], callobj/CALLFRAME_MARSHALCONTEXT, com.callframe_marshalcontext
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CALLFRAME_MARSHALCONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_ICallFrame_0004
 - callobj/__MIDL_ICallFrame_0004
 - CALLFRAME_MARSHALCONTEXT
 - callobj/CALLFRAME_MARSHALCONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - callobj.h
api_name:
 - CALLFRAME_MARSHALCONTEXT
---

## -description

Provides information about the context in which marshalling should be carried out.

## -struct-fields

### -field fIn

<b>TRUE</b> if the in parameter values are to be marshaled and <b>FALSE</b> if the out parameter values are to be marshaled. The in parameter values are marshaled on the client side and the out parameter values are marshaled on the server side.

### -field dwDestContext

Context in which unmarshaling is to be carried out.

### -field pvDestContext

Context in which unmarshaling is to be carried out.

### -field punkReserved

This parameter should be <b>NULL</b>.

### -field guidTransferSyntax

The transfer syntax for which the marshalling should occur.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a>

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>

<a href="/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>