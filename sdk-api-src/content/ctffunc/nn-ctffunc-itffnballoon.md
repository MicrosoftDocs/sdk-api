---
UID: NN:ctffunc.ITfFnBalloon
title: ITfFnBalloon (ctffunc.h)
description: The ITfFnBalloon interface is implemented by a text service and is used by an application or other text service to update the balloon item that the text service adds to the language bar.
helpviewer_keywords: ["ITfFnBalloon","ITfFnBalloon interface [Text Services Framework]","ITfFnBalloon interface [Text Services Framework]","described","_tsf_itffnballoon_ref","ctffunc/ITfFnBalloon","tsf.itffnballoon"]
old-location: tsf\itffnballoon.htm
tech.root: TSF
ms.assetid: 9b79526b-b7e1-41a2-b32e-88124347d77d
ms.date: 12/05/2018
ms.keywords: ITfFnBalloon, ITfFnBalloon interface [Text Services Framework], ITfFnBalloon interface [Text Services Framework],described, _tsf_itffnballoon_ref, ctffunc/ITfFnBalloon, tsf.itffnballoon
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfFnBalloon
 - ctffunc/ITfFnBalloon
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
 - ITfFnBalloon
---

# ITfFnBalloon interface


## -description

The <b>ITfFnBalloon</b> interface is implemented by a text service and is used by an application or other text service to update the balloon item that the text service adds to the language bar.

An application or text service obtains an instance of this interface by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a> with the class identifier of the text service and then calling <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with GUID_NULL and IID_ITfFnBalloon.

## -inheritance

The <b>ITfFnBalloon</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnBalloon</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
