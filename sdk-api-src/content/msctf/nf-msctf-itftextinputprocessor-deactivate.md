---
UID: NF:msctf.ITfTextInputProcessor.Deactivate
title: ITfTextInputProcessor::Deactivate (msctf.h)
description: ITfTextInputProcessor::Deactivate method
helpviewer_keywords: ["Deactivate","Deactivate method [Text Services Framework]","Deactivate method [Text Services Framework]","ITfTextInputProcessor interface","ITfTextInputProcessor interface [Text Services Framework]","Deactivate method","ITfTextInputProcessor.Deactivate","ITfTextInputProcessor::Deactivate","_tsf_itftextinputprocessor_deactivate_ref","msctf/ITfTextInputProcessor::Deactivate","tsf.itftextinputprocessor_deactivate"]
old-location: tsf\itftextinputprocessor_deactivate.htm
tech.root: TSF
ms.assetid: 427190fc-f246-47c6-84e0-a28808a86b6b
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [Text Services Framework], Deactivate method [Text Services Framework],ITfTextInputProcessor interface, ITfTextInputProcessor interface [Text Services Framework],Deactivate method, ITfTextInputProcessor.Deactivate, ITfTextInputProcessor::Deactivate, _tsf_itftextinputprocessor_deactivate_ref, msctf/ITfTextInputProcessor::Deactivate, tsf.itftextinputprocessor_deactivate
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextInputProcessor::Deactivate
 - msctf/ITfTextInputProcessor::Deactivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfTextInputProcessor.Deactivate
---

# ITfTextInputProcessor::Deactivate


## -description

Deactivates a text service when a user session ends.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TSF calls this method immediately before releasing its final reference to a text service. This provides the opportunity to perform operations necessary to shut down the text service.

This method usually unadvises sinks for events that involve the text service. It can also close any user interface elements of the text service.

Before this method returns, it must release all references to the <i>ptim</i> parameter passed to the text service by the <a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itftextinputprocessor">ITfTextInputProcessor
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>
