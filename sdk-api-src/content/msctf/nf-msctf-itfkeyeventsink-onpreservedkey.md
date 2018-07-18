---
UID: NF:msctf.ITfKeyEventSink.OnPreservedKey
title: ITfKeyEventSink::OnPreservedKey
author: windows-sdk-content
description: ITfKeyEventSink::OnPreservedKey method
old-location: tsf\itfkeyeventsink_onpreservedkey.htm
old-project: TSF
ms.assetid: 90b3f2f4-5655-42e3-bdef-62c090800e5e
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfKeyEventSink interface [Text Services Framework],OnPreservedKey method, ITfKeyEventSink.OnPreservedKey, ITfKeyEventSink::OnPreservedKey, OnPreservedKey, OnPreservedKey method [Text Services Framework], OnPreservedKey method [Text Services Framework],ITfKeyEventSink interface, _tsf_itfkeyeventsink_onpreservedkey_ref, msctf/ITfKeyEventSink::OnPreservedKey, tsf.itfkeyeventsink_onpreservedkey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfKeyEventSink.OnPreservedKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfKeyEventSink::OnPreservedKey


## -description




## -parameters




### -param pic [in]

Pointer to the input context that receives the key event.


### -param rguid [in]

Contains the command GUID of the preserved key.


### -param pfEaten [out]

Pointer to a BOOL value that, on exit, indicates if the preserved key event was handled. If this value receives <b>TRUE</b>, the preserved key event was handled. If this value receives <b>FALSE</b>, the preserved key event was not handled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



