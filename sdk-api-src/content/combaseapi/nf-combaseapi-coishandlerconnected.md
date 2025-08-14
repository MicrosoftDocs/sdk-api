---
UID: NF:combaseapi.CoIsHandlerConnected
title: CoIsHandlerConnected function (combaseapi.h)
description: Determines whether a remote object is connected to the corresponding in-process object.
helpviewer_keywords: ["CoIsHandlerConnected","CoIsHandlerConnected function [COM]","_com_CoIsHandlerConnected","com.coishandlerconnected","combaseapi/CoIsHandlerConnected"]
old-location: com\coishandlerconnected.htm
tech.root: com
ms.assetid: f58bdec6-3709-439d-9867-0022a069c53d
ms.date: 12/05/2018
ms.keywords: CoIsHandlerConnected, CoIsHandlerConnected function [COM], _com_CoIsHandlerConnected, com.coishandlerconnected, combaseapi/CoIsHandlerConnected
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - CoIsHandlerConnected
 - combaseapi/CoIsHandlerConnected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoIsHandlerConnected
---

# CoIsHandlerConnected function


## -description

Determines whether a remote object is connected to the corresponding in-process object.

## -parameters

### -param pUnk [in]

A pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the remote object.

## -returns

If the object is not remote or if it is remote and still connected, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.

## -remarks

The <b>CoIsHandlerConnected</b> function determines the status of a remote object. You can use it to determine when to release a remote object. You specify the remote object by giving the function a pointer to its controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface (the <i>pUnk</i> parameter). A value of <b>TRUE</b> returned from the function indicates either that the specified object is not remote, or that it is remote and is still connected to its remote handler. A value of <b>FALSE</b> returned from the function indicates that the object is remote but is no longer connected to its remote handler; in this case, the caller should respond by releasing the object.