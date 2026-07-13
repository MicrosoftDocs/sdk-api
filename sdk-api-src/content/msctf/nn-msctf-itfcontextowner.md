---
UID: NN:msctf.ITfContextOwner
title: ITfContextOwner (msctf.h)
description: The ITfContextOwner interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the ITfSource::AdviseSink method.
helpviewer_keywords: ["ITfContextOwner","ITfContextOwner interface [Text Services Framework]","ITfContextOwner interface [Text Services Framework]","described","_tsf_itfcontextowner_ref","msctf/ITfContextOwner","tsf.itfcontextowner"]
old-location: tsf\itfcontextowner.htm
tech.root: TSF
ms.assetid: 630646df-dd47-4dbf-9787-f9d697ad8d7a
ms.date: 12/05/2018
ms.keywords: ITfContextOwner, ITfContextOwner interface [Text Services Framework], ITfContextOwner interface [Text Services Framework],described, _tsf_itfcontextowner_ref, msctf/ITfContextOwner, tsf.itfcontextowner
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfContextOwner
 - msctf/ITfContextOwner
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
 - ITfContextOwner
---

# ITfContextOwner interface


## -description

The <b>ITfContextOwner</b> interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> method.

## -inheritance

The <b>ITfContextOwner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwner</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
