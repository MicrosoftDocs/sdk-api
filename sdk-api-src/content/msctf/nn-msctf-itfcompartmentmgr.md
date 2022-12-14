---
UID: NN:msctf.ITfCompartmentMgr
title: ITfCompartmentMgr (msctf.h)
description: The ITfCompartmentMgr interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.
helpviewer_keywords: ["ITfCompartmentMgr","ITfCompartmentMgr interface [Text Services Framework]","ITfCompartmentMgr interface [Text Services Framework]","described","_tsf_itfcompartmentmgr_ref","msctf/ITfCompartmentMgr","tsf.itfcompartmentmgr"]
old-location: tsf\itfcompartmentmgr.htm
tech.root: TSF
ms.assetid: 7cdc5c82-4aac-4ec9-b791-93cea33ba8d2
ms.date: 12/05/2018
ms.keywords: ITfCompartmentMgr, ITfCompartmentMgr interface [Text Services Framework], ITfCompartmentMgr interface [Text Services Framework],described, _tsf_itfcompartmentmgr_ref, msctf/ITfCompartmentMgr, tsf.itfcompartmentmgr
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
 - ITfCompartmentMgr
 - msctf/ITfCompartmentMgr
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
 - ITfCompartmentMgr
---

# ITfCompartmentMgr interface


## -description

The <b>ITfCompartmentMgr</b> interface is implemented by the TSF manager and used by clients (applications and text services) to obtain and manipulate TSF compartments.

## -inheritance

The <b>ITfCompartmentMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCompartmentMgr</b> also has these types of members:

## -remarks

The set of compartments that this interface is responsible for depends upon how the interface was obtained. An instance of this interface can be obtained in one of the following ways. For more information, see <a href="/windows/desktop/TSF/compartments">Compartments</a>.

<ul>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getglobalcompartment">ITfThreadMgr::GetGlobalCompartment
            </a> - Obtains the global compartment manager.</li>
<li><b>ITfThreadMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific thread manager.</li>
<li><b>ITfDocumentMgr::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific document manager.</li>
<li><b>ITfContext::QueryInterface</b> with IID_ITfCompartmentMgr - Obtains the compartment manager for this specific context.</li>
</ul>

## -see-also

<a href="/windows/desktop/TSF/compartments">Compartments</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getglobalcompartment">ITfThreadMgr::GetGlobalCompartment
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
