---
UID: NF:ole2.OleCreateDefaultHandler
title: OleCreateDefaultHandler function (ole2.h)
description: Creates a new instance of the default embedding handler. This instance is initialized so it creates a local server when the embedded object enters the running state.
helpviewer_keywords: ["OleCreateDefaultHandler","OleCreateDefaultHandler function [COM]","_ole_OleCreateDefaultHandler","com.olecreatedefaulthandler","ole2/OleCreateDefaultHandler"]
old-location: com\olecreatedefaulthandler.htm
tech.root: com
ms.assetid: ffe87012-b000-4ed7-b0b2-78ffdc794d3b
ms.date: 12/05/2018
ms.keywords: OleCreateDefaultHandler, OleCreateDefaultHandler function [COM], _ole_OleCreateDefaultHandler, com.olecreatedefaulthandler, ole2/OleCreateDefaultHandler
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleCreateDefaultHandler
 - ole2/OleCreateDefaultHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleCreateDefaultHandler
---

# OleCreateDefaultHandler function


## -description

Creates a new instance of the default embedding handler. This instance is initialized so it creates a local server when the embedded object enters the running state.

## -parameters

### -param clsid [in]

CLSID identifying the OLE server to be loaded when the embedded object enters the running state.

### -param pUnkOuter [in]

 Pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface if the handler is to be aggregated; <b>NULL</b> if it is not to be aggregated.

### -param riid [in]

Reference to the identifier of the interface, usually IID_IOleObject, through which the caller will communicate with the handler.

### -param lplpObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created handler.

## -returns

This function returns NOERROR on success and supports the standard return value E_OUTOFMEMORY.

## -remarks

<b>OleCreateDefaultHandler</b> creates a new instance of the default embedding handler, initialized so it creates a local server identified by the <i>clsid</i> parameter when the embedded object enters the running state. If you are writing a handler and want to use the services of the default handler, call <b>OleCreateDefaultHandler</b>. OLE also calls it internally when the CLSID specified in an object creation call is not registered.



If the given class does not have a special handler, a call to <b>OleCreateDefaultHandler</b> produces the same results as a call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function with the class context parameter assigned the value CLSCTX_INPROC_HANDLER.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>