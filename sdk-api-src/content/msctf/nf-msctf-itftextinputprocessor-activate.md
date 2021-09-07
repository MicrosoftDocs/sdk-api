---
UID: NF:msctf.ITfTextInputProcessor.Activate
title: ITfTextInputProcessor::Activate (msctf.h)
description: ITfTextInputProcessor::Activate method
helpviewer_keywords: ["Activate","Activate method [Text Services Framework]","Activate method [Text Services Framework]","ITfTextInputProcessor interface","ITfTextInputProcessor interface [Text Services Framework]","Activate method","ITfTextInputProcessor.Activate","ITfTextInputProcessor::Activate","_tsf_itftextinputprocessor_activate_ref","msctf/ITfTextInputProcessor::Activate","tsf.itftextinputprocessor_activate"]
old-location: tsf\itftextinputprocessor_activate.htm
tech.root: TSF
ms.assetid: c5fd6b5c-0a78-4b5b-aad5-0c398798cf30
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Text Services Framework], Activate method [Text Services Framework],ITfTextInputProcessor interface, ITfTextInputProcessor interface [Text Services Framework],Activate method, ITfTextInputProcessor.Activate, ITfTextInputProcessor::Activate, _tsf_itftextinputprocessor_activate_ref, msctf/ITfTextInputProcessor::Activate, tsf.itftextinputprocessor_activate
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
 - ITfTextInputProcessor::Activate
 - msctf/ITfTextInputProcessor::Activate
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
 - ITfTextInputProcessor.Activate
---

# ITfTextInputProcessor::Activate


## -description

Activates a text service when a user session starts.

## -parameters

### -param ptim [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a> interface for the thread manager that owns the text service.

### -param tid [in]

Specifies the client identifier for the text service.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TSF calls this method after creating an instance of a text service with a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. This enables operations necessary to start the text service.

This method usually adds a reference to the thread manager for the session and advise sinks for events that involve the text service, such as change of focus, keystrokes, and window events. It also customizes the language bar for the text service.

The corresponding <a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate">ITfTextInputProcessor::Deactivate</a> method that shuts down the text service must release all references to the <i>ptim</i> parameter.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itftextinputprocessor">ITfTextInputProcessor
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate">ITfTextInputProcessor::Deactivate
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>