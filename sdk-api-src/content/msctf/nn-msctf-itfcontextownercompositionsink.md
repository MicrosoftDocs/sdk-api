---
UID: NN:msctf.ITfContextOwnerCompositionSink
title: ITfContextOwnerCompositionSink (msctf.h)
description: The ITfContextOwnerCompositionSink interface is implemented by an application to receive composition-related notifications.
helpviewer_keywords: ["ITfContextOwnerCompositionSink","ITfContextOwnerCompositionSink interface [Text Services Framework]","ITfContextOwnerCompositionSink interface [Text Services Framework]","described","_tsf_itfcontextownercompositionsink_ref","msctf/ITfContextOwnerCompositionSink","tsf.itfcontextownercompositionsink"]
old-location: tsf\itfcontextownercompositionsink.htm
tech.root: TSF
ms.assetid: 4fea0a48-df5f-4f34-a3ea-d52883f6f8b1
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionSink, ITfContextOwnerCompositionSink interface [Text Services Framework], ITfContextOwnerCompositionSink interface [Text Services Framework],described, _tsf_itfcontextownercompositionsink_ref, msctf/ITfContextOwnerCompositionSink, tsf.itfcontextownercompositionsink
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
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerCompositionSink
 - msctf/ITfContextOwnerCompositionSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwnerCompositionSink
---

# ITfContextOwnerCompositionSink interface


## -description

The <b>ITfContextOwnerCompositionSink</b> interface is implemented by an application to receive composition-related notifications. When the application calls <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>, the TSF manager queries the object for this interface. If the object supports this interface, the advise sink is installed.

## -inheritance

The <b>ITfContextOwnerCompositionSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwnerCompositionSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
