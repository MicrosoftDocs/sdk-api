---
UID: NN:msctf.ITfEditRecord
title: ITfEditRecord (msctf.h)
description: The ITfEditRecord interface is implemented by the TSF manager and is used by a text edit sink to determine what was changed during an edit session.
helpviewer_keywords: ["ITfEditRecord","ITfEditRecord interface [Text Services Framework]","ITfEditRecord interface [Text Services Framework]","described","_tsf_itfeditrecord_ref","msctf/ITfEditRecord","tsf.itfeditrecord"]
old-location: tsf\itfeditrecord.htm
tech.root: TSF
ms.assetid: 2106cd97-9e1f-4d7c-a7a4-55676cf8923b
ms.date: 12/05/2018
ms.keywords: ITfEditRecord, ITfEditRecord interface [Text Services Framework], ITfEditRecord interface [Text Services Framework],described, _tsf_itfeditrecord_ref, msctf/ITfEditRecord, tsf.itfeditrecord
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
 - ITfEditRecord
 - msctf/ITfEditRecord
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
 - ITfEditRecord
---

# ITfEditRecord interface


## -description

The <b>ITfEditRecord</b> interface is implemented by the TSF manager and is used by a text edit sink to determine what was changed during an edit session. An instance of this interface is passed to the text edit sink when the <a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> method is called.

## -inheritance

The <b>ITfEditRecord</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfEditRecord</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
