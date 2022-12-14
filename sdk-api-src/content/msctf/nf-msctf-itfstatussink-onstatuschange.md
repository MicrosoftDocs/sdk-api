---
UID: NF:msctf.ITfStatusSink.OnStatusChange
title: ITfStatusSink::OnStatusChange (msctf.h)
description: ITfStatusSink::OnStatusChange method
helpviewer_keywords: ["ITfStatusSink interface [Text Services Framework]","OnStatusChange method","ITfStatusSink.OnStatusChange","ITfStatusSink::OnStatusChange","OnStatusChange","OnStatusChange method [Text Services Framework]","OnStatusChange method [Text Services Framework]","ITfStatusSink interface","_tsf_itfstatussink_onstatuschange_ref","msctf/ITfStatusSink::OnStatusChange","tsf.itfstatussink_onstatuschange"]
old-location: tsf\itfstatussink_onstatuschange.htm
tech.root: TSF
ms.assetid: 6eabf08f-006b-43b4-aea7-1d803b3d09b2
ms.date: 12/05/2018
ms.keywords: ITfStatusSink interface [Text Services Framework],OnStatusChange method, ITfStatusSink.OnStatusChange, ITfStatusSink::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITfStatusSink interface, _tsf_itfstatussink_onstatuschange_ref, msctf/ITfStatusSink::OnStatusChange, tsf.itfstatussink_onstatuschange
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
 - ITfStatusSink::OnStatusChange
 - msctf/ITfStatusSink::OnStatusChange
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
 - ITfStatusSink.OnStatusChange
---

# ITfStatusSink::OnStatusChange


## -description

Receives a notification when one of the dynamic flags of the TF_STATUS structure changes.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface whose status has changed.

### -param dwFlags [in]

Indicates that one of the dynamic flags changed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method receives a callback when one of the flags of the <b>dwDynamicFlags</b> member of the <b>TF_STATUS</b> structure changes value. To obtain the changed flag(s), use the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getstatus">ITfContext::GetStatus</a> method.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getstatus">ITfContext::GetStatus
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfstatussink">ITfStatusSink</a>



<a href="/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)">TF_STATUS
      </a>