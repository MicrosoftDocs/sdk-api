---
UID: NN:msctf.ITfReadOnlyProperty
title: ITfReadOnlyProperty (msctf.h)
description: The ITfReadOnlyProperty interface is implemented by the TSF manager and used by an application or text service to obtain property data.
helpviewer_keywords: ["ITfReadOnlyProperty","ITfReadOnlyProperty interface [Text Services Framework]","ITfReadOnlyProperty interface [Text Services Framework]","described","_tsf_itfreadonlyproperty_ref","msctf/ITfReadOnlyProperty","tsf.itfreadonlyproperty"]
old-location: tsf\itfreadonlyproperty.htm
tech.root: TSF
ms.assetid: f4021a3d-6b86-469f-8943-770e7ef0cf99
ms.date: 12/05/2018
ms.keywords: ITfReadOnlyProperty, ITfReadOnlyProperty interface [Text Services Framework], ITfReadOnlyProperty interface [Text Services Framework],described, _tsf_itfreadonlyproperty_ref, msctf/ITfReadOnlyProperty, tsf.itfreadonlyproperty
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
 - ITfReadOnlyProperty
 - msctf/ITfReadOnlyProperty
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
 - ITfReadOnlyProperty
---

# ITfReadOnlyProperty interface


## -description

The <b>ITfReadOnlyProperty</b> interface is implemented by the TSF manager and used by an application or text service to obtain property data.

## -inheritance

The <b>ITfReadOnlyProperty</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReadOnlyProperty</b> also has these types of members:

## -remarks

An instance of this interface is obtained by using <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">ITfContext::GetAppProperty</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">ITfContext::TrackProperties</a>.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">ITfContext::GetAppProperty
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-trackproperties">ITfContext::TrackProperties
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
