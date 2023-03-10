---
UID: NN:msctf.ITfCompartment
title: ITfCompartment (msctf.h)
description: The ITfCompartment interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.
helpviewer_keywords: ["ITfCompartment","ITfCompartment interface [Text Services Framework]","ITfCompartment interface [Text Services Framework]","described","_tsf_itfcompartment_ref","msctf/ITfCompartment","tsf.itfcompartment"]
old-location: tsf\itfcompartment.htm
tech.root: TSF
ms.assetid: c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3
ms.date: 12/05/2018
ms.keywords: ITfCompartment, ITfCompartment interface [Text Services Framework], ITfCompartment interface [Text Services Framework],described, _tsf_itfcompartment_ref, msctf/ITfCompartment, tsf.itfcompartment
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
 - ITfCompartment
 - msctf/ITfCompartment
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
 - ITfCompartment
---

# ITfCompartment interface


## -description

The <b>ITfCompartment</b> interface is implemented by the TSF manager and is used by clients (applications and text services) to obtain and set data in a TSF compartment.

A client also uses this interface to obtain an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface that is used to install an <a href="/windows/desktop/api/msctf/nn-msctf-itfcompartmenteventsink">ITfCompartmentEventSink</a> compartment change notification sink. The client calls <b>ITfCompartment::QueryInterface</b> with IID_ITfSource to obtain the <b>ITfSource</b> interface.

## -inheritance

The <b>ITfCompartment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompartment</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TSF/compartments">Compartments</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
