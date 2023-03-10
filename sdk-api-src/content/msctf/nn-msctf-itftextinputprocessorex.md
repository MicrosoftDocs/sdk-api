---
UID: NN:msctf.ITfTextInputProcessorEx
title: ITfTextInputProcessorEx (msctf.h)
description: The ITfTextInputProcessorEx interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service.
helpviewer_keywords: ["ITfTextInputProcessorEx","ITfTextInputProcessorEx interface [Text Services Framework]","ITfTextInputProcessorEx interface [Text Services Framework]","described","_tsf_itftextinputprocessorex_ref","msctf/ITfTextInputProcessorEx","tsf.itftextinputprocessorex"]
old-location: tsf\itftextinputprocessorex.htm
tech.root: TSF
ms.assetid: fc762a6f-8d15-4082-9588-fc77fa565549
ms.date: 12/05/2018
ms.keywords: ITfTextInputProcessorEx, ITfTextInputProcessorEx interface [Text Services Framework], ITfTextInputProcessorEx interface [Text Services Framework],described, _tsf_itftextinputprocessorex_ref, msctf/ITfTextInputProcessorEx, tsf.itftextinputprocessorex
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextInputProcessorEx
 - msctf/ITfTextInputProcessorEx
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
 - ITfTextInputProcessorEx
---

# ITfTextInputProcessorEx interface


## -description

The <b>ITfTextInputProcessorEx</b> interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service. The manager obtains a pointer to this interface when it creates an instance of the text service for a thread with a call to CoCreateInstance.

## -inheritance

The <b>ITfTextInputProcessorEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfTextInputProcessorEx</b> also has these types of members:

