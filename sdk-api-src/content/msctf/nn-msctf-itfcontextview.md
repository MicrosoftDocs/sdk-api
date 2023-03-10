---
UID: NN:msctf.ITfContextView
title: ITfContextView (msctf.h)
description: The ITfContextView interface is implemented by the TSF manager and used by a client (application or text service) to obtain information about a context view.
helpviewer_keywords: ["ITfContextView","ITfContextView interface [Text Services Framework]","ITfContextView interface [Text Services Framework]","described","_tsf_itfcontextview_ref","msctf/ITfContextView","tsf.itfcontextview"]
old-location: tsf\itfcontextview.htm
tech.root: TSF
ms.assetid: 302d185d-dab7-4a77-a5cf-da2529d8b24a
ms.date: 12/05/2018
ms.keywords: ITfContextView, ITfContextView interface [Text Services Framework], ITfContextView interface [Text Services Framework],described, _tsf_itfcontextview_ref, msctf/ITfContextView, tsf.itfcontextview
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
 - ITfContextView
 - msctf/ITfContextView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextView
---

# ITfContextView interface


## -description

The <b>ITfContextView</b> interface is implemented by the TSF manager and used by a client (application or text service) to obtain information about a context view. Clients obtain this interface by calling the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getactiveview">ITfContext::GetActiveView</a> method which returns a pointer to the <b>ITfContextView</b> object.

## -inheritance

The <b>ITfContextView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextView</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
