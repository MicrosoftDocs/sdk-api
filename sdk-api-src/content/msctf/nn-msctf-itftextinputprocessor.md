---
UID: NN:msctf.ITfTextInputProcessor
title: ITfTextInputProcessor (msctf.h)
description: The ITfTextInputProcessor interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service.
helpviewer_keywords: ["ITfTextInputProcessor","ITfTextInputProcessor interface [Text Services Framework]","ITfTextInputProcessor interface [Text Services Framework]","described","_tsf_itftextinputprocessor_ref","msctf/ITfTextInputProcessor","tsf.itftextinputprocessor"]
old-location: tsf\itftextinputprocessor.htm
tech.root: TSF
ms.assetid: d3fd296b-0009-4fc2-bf91-0ad31454f0e8
ms.date: 12/05/2018
ms.keywords: ITfTextInputProcessor, ITfTextInputProcessor interface [Text Services Framework], ITfTextInputProcessor interface [Text Services Framework],described, _tsf_itftextinputprocessor_ref, msctf/ITfTextInputProcessor, tsf.itftextinputprocessor
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
req.dll: Sptip.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextInputProcessor
 - msctf/ITfTextInputProcessor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sptip.dll
api_name:
 - ITfTextInputProcessor
---

# ITfTextInputProcessor interface


## -description

The <b>ITfTextInputProcessor</b> interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service. The manager obtains a pointer to this interface when it creates an instance of the text service for a thread with a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>.

## -inheritance

The <b>ITfTextInputProcessor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTextInputProcessor</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
