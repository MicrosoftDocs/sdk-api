---
UID: NN:ctffunc.ITfLMLattice
title: ITfLMLattice (ctffunc.h)
description: The ITfLMLattice interface is implemented by the speech text service to provide information about lattice element properties and is used by a client (application or other text service).
helpviewer_keywords: ["ITfLMLattice","ITfLMLattice interface [Text Services Framework]","ITfLMLattice interface [Text Services Framework]","described","_tsf_itflmlattice_ref","ctffunc/ITfLMLattice","tsf.itflmlattice"]
old-location: tsf\itflmlattice.htm
tech.root: TSF
ms.assetid: 25ad6ef2-1d42-498a-852f-163a0efbc26a
ms.date: 12/05/2018
ms.keywords: ITfLMLattice, ITfLMLattice interface [Text Services Framework], ITfLMLattice interface [Text Services Framework],described, _tsf_itflmlattice_ref, ctffunc/ITfLMLattice, tsf.itflmlattice
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfLMLattice
 - ctffunc/ITfLMLattice
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
 - ITfLMLattice
---

# ITfLMLattice interface


## -description

The <b>ITfLMLattice</b> interface is implemented by the speech text service to provide information about lattice element properties and is used by a client (application or other text service). A client obtains this interface from the GUID_PROP_LMLATTICE property by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue">ITfReadOnlyProperty::GetValue</a>. For more information, see <a href="/windows/desktop/TSF/predefined-properties">Predefined Properties</a>.

## -inheritance

The <b>ITfLMLattice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLMLattice</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue">ITfReadOnlyProperty::GetValue
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/predefined-properties">Predefined Properties
      </a>
