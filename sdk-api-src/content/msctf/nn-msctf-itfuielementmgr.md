---
UID: NN:msctf.ITfUIElementMgr
title: ITfUIElementMgr (msctf.h)
description: The ITfUIElementMgr interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.
helpviewer_keywords: ["ITfUIElementMgr","ITfUIElementMgr interface [Text Services Framework]","ITfUIElementMgr interface [Text Services Framework]","described","_tsf_itfuielementmgr_ref","msctf/ITfUIElementMgr","tsf.itfuielementmgr"]
old-location: tsf\itfuielementmgr.htm
tech.root: TSF
ms.assetid: 7b4d3f4e-bf30-45c6-8709-88b71b25d333
ms.date: 12/05/2018
ms.keywords: ITfUIElementMgr, ITfUIElementMgr interface [Text Services Framework], ITfUIElementMgr interface [Text Services Framework],described, _tsf_itfuielementmgr_ref, msctf/ITfUIElementMgr, tsf.itfuielementmgr
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfUIElementMgr
 - msctf/ITfUIElementMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfUIElementMgr
---

# ITfUIElementMgr interface


## -description

The <b>ITfUIElementMgr</b> interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.

## -inheritance

The <b>ITfUIElementMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfUIElementMgr</b> also has these types of members:

## -remarks

A text service that supports UIElement must call <b>ITfUIElementMgr</b> whenever the UI is shown, updated or hidden. Then the application can control the visibility of the UI.
