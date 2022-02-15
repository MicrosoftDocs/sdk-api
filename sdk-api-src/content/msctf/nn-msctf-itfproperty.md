---
UID: NN:msctf.ITfProperty
title: ITfProperty (msctf.h)
description: The ITfProperty interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.
helpviewer_keywords: ["ITfProperty","ITfProperty interface [Text Services Framework]","ITfProperty interface [Text Services Framework]","described","_tsf_itfproperty_ref","msctf/ITfProperty","tsf.itfproperty"]
old-location: tsf\itfproperty.htm
tech.root: TSF
ms.assetid: 72bd92f9-d82e-4994-82ad-0989e987903b
ms.date: 12/05/2018
ms.keywords: ITfProperty, ITfProperty interface [Text Services Framework], ITfProperty interface [Text Services Framework],described, _tsf_itfproperty_ref, msctf/ITfProperty, tsf.itfproperty
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
 - ITfProperty
 - msctf/ITfProperty
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
 - ITfProperty
---

# ITfProperty interface


## -description

The <b>ITfProperty</b> interface is implemented by the TSF manager and used by a client (application or text service) to modify a property value.

## -inheritance

The <b>ITfProperty</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfProperty</b> also has these types of members:

## -remarks

An instance of this interface is obtained in various ways, such as <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty</a> or <a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next">IEnumTfProperties::Next</a>.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next">IEnumTfProperties::Next
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
