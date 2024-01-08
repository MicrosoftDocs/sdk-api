---
UID: NF:shellhandwriting.RegisterHandwritingInputRoutingCallback
tech.root: input_ink
title: RegisterHandwritingInputRoutingCallback
ms.date: 10/24/2023
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shellhandwriting.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - shellhandwriting.h
api_name:
 - RegisterHandwritingInputRoutingCallback
f1_keywords:
 - RegisterHandwritingInputRoutingCallback
 - shellhandwriting/RegisterHandwritingInputRoutingCallback
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterHandwritingInputRoutingCallback
---

# RegisterHandwritingInputRoutingCallback function

## -description

Registers an [IHandwritingInputRoutingCallback](nn-shellhandwriting-ihandwritinginputroutingcallback.md).

## -parameters

### -param callback [in]

The [IHandwritingInputRoutingCallback](nn-shellhandwriting-ihandwritinginputroutingcallback.md) being registered.

## -returns

If the method succeeds, it returns **S_OK**. If it fails, it returns an **HRESULT** error code.

## -remarks

## -see-also

