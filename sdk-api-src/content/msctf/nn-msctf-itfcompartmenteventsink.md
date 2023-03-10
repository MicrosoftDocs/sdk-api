---
UID: NN:msctf.ITfCompartmentEventSink
title: ITfCompartmentEventSink (msctf.h)
description: The ITfCompartmentEventSink interface is implemented by a client (application or text service) and used by the TSF manager to notify the client when compartment data changes.
helpviewer_keywords: ["ITfCompartmentEventSink","ITfCompartmentEventSink interface [Text Services Framework]","ITfCompartmentEventSink interface [Text Services Framework]","described","_tsf_itfcompartmenteventsink_ref","msctf/ITfCompartmentEventSink","tsf.itfcompartmenteventsink"]
old-location: tsf\itfcompartmenteventsink.htm
tech.root: TSF
ms.assetid: 1bd464e7-9e34-4725-83f9-42e09ddf4778
ms.date: 12/05/2018
ms.keywords: ITfCompartmentEventSink, ITfCompartmentEventSink interface [Text Services Framework], ITfCompartmentEventSink interface [Text Services Framework],described, _tsf_itfcompartmenteventsink_ref, msctf/ITfCompartmentEventSink, tsf.itfcompartmenteventsink
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCompartmentEventSink
 - msctf/ITfCompartmentEventSink
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
 - ITfCompartmentEventSink
---

# ITfCompartmentEventSink interface


## -description

The <b>ITfCompartmentEventSink</b> interface is implemented by a client (application or text service) and used by the TSF manager to notify the client when compartment data changes. This notification sink is installed by obtaining an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface from the <a href="/windows/desktop/api/msctf/nn-msctf-itfcompartment">ITfCompartment</a> object and calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfCompartmentEventSink and a pointer to the <b>ITfCompartmentEventSink</b> object.

## -inheritance

The <b>ITfCompartmentEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompartmentEventSink</b> also has these types of members:

