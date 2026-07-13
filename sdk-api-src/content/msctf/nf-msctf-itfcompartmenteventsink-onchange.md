---
UID: NF:msctf.ITfCompartmentEventSink.OnChange
title: ITfCompartmentEventSink::OnChange (msctf.h)
description: ITfCompartmentEventSink::OnChange method
helpviewer_keywords: ["ITfCompartmentEventSink interface [Text Services Framework]","OnChange method","ITfCompartmentEventSink.OnChange","ITfCompartmentEventSink::OnChange","OnChange","OnChange method [Text Services Framework]","OnChange method [Text Services Framework]","ITfCompartmentEventSink interface","_tsf_itfcompartmenteventsink_onchange_ref","msctf/ITfCompartmentEventSink::OnChange","tsf.itfcompartmenteventsink_onchange"]
old-location: tsf\itfcompartmenteventsink_onchange.htm
tech.root: TSF
ms.assetid: 1756754c-6353-4296-bdb5-1cbef1d29ec5
ms.date: 12/05/2018
ms.keywords: ITfCompartmentEventSink interface [Text Services Framework],OnChange method, ITfCompartmentEventSink.OnChange, ITfCompartmentEventSink::OnChange, OnChange, OnChange method [Text Services Framework], OnChange method [Text Services Framework],ITfCompartmentEventSink interface, _tsf_itfcompartmenteventsink_onchange_ref, msctf/ITfCompartmentEventSink::OnChange, tsf.itfcompartmenteventsink_onchange
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
 - ITfCompartmentEventSink::OnChange
 - msctf/ITfCompartmentEventSink::OnChange
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
 - ITfCompartmentEventSink.OnChange
---

# ITfCompartmentEventSink::OnChange


## -description

Called when compartment data changes.

## -parameters

### -param rguid [in]

Contains a GUID that identifies the compartment that changed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When this method is called, the data has changed. The new data can be obtained at this time by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfcompartment-getvalue">ITfCompartment::GetValue</a>.

<a href="/windows/desktop/api/msctf/nf-msctf-itfcompartment-setvalue">ITfCompartment::SetValue</a> will return E_UNEXPECTED if called from within this notification.

## -see-also

[ITfCompartment::GetValue](nf-msctf-itfcompartment-getvalue.md), [ITfCompartment::SetValue](nf-msctf-itfcompartment-setvalue.md), [ITfCompartmentEventSink interface](nn-msctf-itfcompartmenteventsink.md)