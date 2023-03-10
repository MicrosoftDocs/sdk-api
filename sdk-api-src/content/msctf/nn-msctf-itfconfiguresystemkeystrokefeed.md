---
UID: NN:msctf.ITfConfigureSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed (msctf.h)
description: The ITfConfigureSystemKeystrokeFeed interface is implemented by the TSF manager to enable and disable the processing of keystrokes.
helpviewer_keywords: ["ITfConfigureSystemKeystrokeFeed","ITfConfigureSystemKeystrokeFeed interface [Text Services Framework]","ITfConfigureSystemKeystrokeFeed interface [Text Services Framework]","described","_tsf_itfconfiguresystemkeystrokefeed_ref","msctf/ITfConfigureSystemKeystrokeFeed","tsf.itfconfiguresystemkeystrokefeed"]
old-location: tsf\itfconfiguresystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 9b15d628-87aa-4e20-b9c3-fb29a79683cb
ms.date: 12/05/2018
ms.keywords: ITfConfigureSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework], ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],described, _tsf_itfconfiguresystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed
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
 - ITfConfigureSystemKeystrokeFeed
 - msctf/ITfConfigureSystemKeystrokeFeed
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
 - ITfConfigureSystemKeystrokeFeed
---

# ITfConfigureSystemKeystrokeFeed interface


## -description

The <b>ITfConfigureSystemKeystrokeFeed</b> interface is implemented by the TSF manager to enable and disable the processing of keystrokes. This interface is obtained by calling the TSF manager's <b>ITfThreadMgr::QueryInterface</b> with IID_ITfConfigureSystemKeystrokeFeed.

## -inheritance

The <b>ITfConfigureSystemKeystrokeFeed</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfConfigureSystemKeystrokeFeed</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
