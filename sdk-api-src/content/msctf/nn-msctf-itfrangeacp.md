---
UID: NN:msctf.ITfRangeACP
title: ITfRangeACP (msctf.h)
description: The ITfRangeACP interface is implemented by the TSF manager and is used by an application character position (ACP)-based application to access and manipulate range objects.
helpviewer_keywords: ["ITfRangeACP","ITfRangeACP interface [Text Services Framework]","ITfRangeACP interface [Text Services Framework]","described","_tsf_itfrangeacp_ref","msctf/ITfRangeACP","tsf.itfrangeacp"]
old-location: tsf\itfrangeacp.htm
tech.root: TSF
ms.assetid: aaa497ca-4cf2-401a-a6d8-cc8a75479cc4
ms.date: 12/05/2018
ms.keywords: ITfRangeACP, ITfRangeACP interface [Text Services Framework], ITfRangeACP interface [Text Services Framework],described, _tsf_itfrangeacp_ref, msctf/ITfRangeACP, tsf.itfrangeacp
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
 - ITfRangeACP
 - msctf/ITfRangeACP
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
 - ITfRangeACP
---

# ITfRangeACP interface


## -description

The <b>ITfRangeACP</b> interface is implemented by the TSF manager and is used by an application character position (ACP)-based application to access and manipulate range objects. This interface is derived from the <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface. Obtain an instance of this interface by querying an <b>ITfRange</b> object for IID_ITfRangeACP.

## -inheritance

The <b>ITfRangeACP</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfRangeACP</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
