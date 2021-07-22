---
UID: NN:msctf.ITfDisplayAttributeProvider
title: ITfDisplayAttributeProvider (msctf.h)
description: The ITfDisplayAttributeProvider interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.
helpviewer_keywords: ["ITfDisplayAttributeProvider","ITfDisplayAttributeProvider interface [Text Services Framework]","ITfDisplayAttributeProvider interface [Text Services Framework]","described","_tsf_itfdisplayattributeprovider_ref","msctf/ITfDisplayAttributeProvider","tsf.itfdisplayattributeprovider"]
old-location: tsf\itfdisplayattributeprovider.htm
tech.root: TSF
ms.assetid: c0346d5e-d4a2-4c72-90be-de5ff1681acd
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeProvider, ITfDisplayAttributeProvider interface [Text Services Framework], ITfDisplayAttributeProvider interface [Text Services Framework],described, _tsf_itfdisplayattributeprovider_ref, msctf/ITfDisplayAttributeProvider, tsf.itfdisplayattributeprovider
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
req.dll: Imjpcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDisplayAttributeProvider
 - msctf/ITfDisplayAttributeProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imjpcic.dll
api_name:
 - ITfDisplayAttributeProvider
---

# ITfDisplayAttributeProvider interface


## -description

The <b>ITfDisplayAttributeProvider</b> interface is implemented by a text service and is used by the TSF manager to enumerate and obtain individual display attribute information objects.

The TSF manager obtains an instance of this interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the class identifier passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory</a> with GUID_TFCAT_DISPLAYATTRIBUTEPROVIDER and IID_ITfDisplayAttributeProvider. For more information, see <a href="/windows/desktop/TSF/providing-display-attributes">Providing Display Attributes</a>.

## -inheritance

The <b>ITfDisplayAttributeProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/providing-display-attributes">Providing Display Attributes</a>
