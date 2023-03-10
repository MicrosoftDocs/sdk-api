---
UID: NF:msctf.ITfKeyEventSink.OnPreservedKey
title: ITfKeyEventSink::OnPreservedKey (msctf.h)
description: ITfKeyEventSink::OnPreservedKey method
helpviewer_keywords: ["ITfKeyEventSink interface [Text Services Framework]","OnPreservedKey method","ITfKeyEventSink.OnPreservedKey","ITfKeyEventSink::OnPreservedKey","OnPreservedKey","OnPreservedKey method [Text Services Framework]","OnPreservedKey method [Text Services Framework]","ITfKeyEventSink interface","_tsf_itfkeyeventsink_onpreservedkey_ref","msctf/ITfKeyEventSink::OnPreservedKey","tsf.itfkeyeventsink_onpreservedkey"]
old-location: tsf\itfkeyeventsink_onpreservedkey.htm
tech.root: TSF
ms.assetid: 90b3f2f4-5655-42e3-bdef-62c090800e5e
ms.date: 12/05/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnPreservedKey method, ITfKeyEventSink.OnPreservedKey, ITfKeyEventSink::OnPreservedKey, OnPreservedKey, OnPreservedKey method [Text Services Framework], OnPreservedKey method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_onpreservedkey_ref, msctf/ITfKeyEventSink::OnPreservedKey, tsf.itfkeyeventsink_onpreservedkey
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfKeyEventSink::OnPreservedKey
 - msctf/ITfKeyEventSink::OnPreservedKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeyEventSink.OnPreservedKey
---

# ITfKeyEventSink::OnPreservedKey


## -description

Called when a preserved key event occurs.

## -parameters

### -param pic [in]

Pointer to the input context that receives the key event.

### -param rguid [in]

Contains the command GUID of the preserved key.

### -param pfEaten [out]

Pointer to a BOOL value that, on exit, indicates if the preserved key event was handled. If this value receives <b>TRUE</b>, the preserved key event was handled. If this value receives <b>FALSE</b>, the preserved key event was not handled.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

