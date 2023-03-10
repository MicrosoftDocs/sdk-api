---
UID: NN:ctffunc.ITfFnAdviseText
title: ITfFnAdviseText (ctffunc.h)
description: The ITfFnAdviseText interface is implemented by a text service and used by the TSF manager to supply notifications when the text or lattice element in a context changes.
helpviewer_keywords: ["ITfFnAdviseText","ITfFnAdviseText interface [Text Services Framework]","ITfFnAdviseText interface [Text Services Framework]","described","_tsf_itffnadvisetext_ref","ctffunc/ITfFnAdviseText","tsf.itffnadvisetext"]
old-location: tsf\itffnadvisetext.htm
tech.root: TSF
ms.assetid: 7cca7f23-48d3-4855-8f3d-e937bbc990d4
ms.date: 12/05/2018
ms.keywords: ITfFnAdviseText, ITfFnAdviseText interface [Text Services Framework], ITfFnAdviseText interface [Text Services Framework],described, _tsf_itffnadvisetext_ref, ctffunc/ITfFnAdviseText, tsf.itffnadvisetext
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
 - ITfFnAdviseText
 - ctffunc/ITfFnAdviseText
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
 - ITfFnAdviseText
---

# ITfFnAdviseText interface


## -description

The <b>ITfFnAdviseText</b> interface is implemented by a text service and used by the TSF manager to supply notifications when the text or lattice element in a context changes.

The manager obtains this interface from the text service by calling the text service <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnAdviseText.

## -inheritance

The <b>ITfFnAdviseText</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnAdviseText</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
