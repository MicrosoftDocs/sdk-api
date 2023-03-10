---
UID: NN:msctf.ITfDisplayAttributeInfo
title: ITfDisplayAttributeInfo (msctf.h)
description: The ITfDisplayAttributeInfo interface is implemented by a text service to provide display attribute data. This interface is used by any component, most often an application, that must determine how text displays.
helpviewer_keywords: ["ITfDisplayAttributeInfo","ITfDisplayAttributeInfo interface [Text Services Framework]","ITfDisplayAttributeInfo interface [Text Services Framework]","described","_tsf_itfdisplayattributeinfo_ref","msctf/ITfDisplayAttributeInfo","tsf.itfdisplayattributeinfo"]
old-location: tsf\itfdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 7f590ecf-06e9-42da-ba40-4364296ae594
ms.date: 12/05/2018
ms.keywords: ITfDisplayAttributeInfo, ITfDisplayAttributeInfo interface [Text Services Framework], ITfDisplayAttributeInfo interface [Text Services Framework],described, _tsf_itfdisplayattributeinfo_ref, msctf/ITfDisplayAttributeInfo, tsf.itfdisplayattributeinfo
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
 - ITfDisplayAttributeInfo
 - msctf/ITfDisplayAttributeInfo
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
 - ITfDisplayAttributeInfo
---

# ITfDisplayAttributeInfo interface


## -description

The <b>ITfDisplayAttributeInfo</b> interface is implemented by a text service to provide display attribute data. This interface is used by any component, most often an application, that must determine how text displays.

## -inheritance

The <b>ITfDisplayAttributeInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfDisplayAttributeInfo</b> also has these types of members:

## -remarks

An application obtains an instance of this interface by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</a> or <a href="/windows/desktop/api/msctf/nf-msctf-ienumtfdisplayattributeinfo-next">IEnumTfDisplayAttributeInfo::Next</a>.

A text service supplies an instance of this interface in its <a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</a> method.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-ienumtfdisplayattributeinfo-next">IEnumTfDisplayAttributeInfo::Next
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo">ITfDisplayAttributeMgr::GetDisplayAttributeInfo
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo">ITfDisplayAttributeProvider::GetDisplayAttributeInfo
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
