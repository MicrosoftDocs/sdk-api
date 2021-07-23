---
UID: NN:ctfutb.ITfSystemLangBarItemSink
title: ITfSystemLangBarItemSink (ctfutb.h)
description: The ITfSystemLangBarItemSink interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu.
helpviewer_keywords: ["ITfSystemLangBarItemSink","ITfSystemLangBarItemSink interface [Text Services Framework]","ITfSystemLangBarItemSink interface [Text Services Framework]","described","_tsf_itfsystemlangbaritemsink_ref","ctfutb/ITfSystemLangBarItemSink","tsf.itfsystemlangbaritemsink"]
old-location: tsf\itfsystemlangbaritemsink.htm
tech.root: TSF
ms.assetid: a88b20ec-fc54-4814-9ca1-131664b4f377
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItemSink, ITfSystemLangBarItemSink interface [Text Services Framework], ITfSystemLangBarItemSink interface [Text Services Framework],described, _tsf_itfsystemlangbaritemsink_ref, ctfutb/ITfSystemLangBarItemSink, tsf.itfsystemlangbaritemsink
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - ITfSystemLangBarItemSink
 - ctfutb/ITfSystemLangBarItemSink
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
 - ITfSystemLangBarItemSink
---

# ITfSystemLangBarItemSink interface


## -description

The <b>ITfSystemLangBarItemSink</b> interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu. The extension obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object with IID_ITfSystemLangBarItemSink. It can then pass the object to the host by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>.

## -inheritance

The <b>ITfSystemLangBarItemSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSystemLangBarItemSink</b> also has these types of members:

## -remarks

A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <b>ITfSource::AdviseSink</b> implementation. The system item should also implement the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritem">ITfSystemLangBarItem</a> interface. The system item uses the <b>ITfSystemLangBarItemSink</b> interface to allow the extension to add its items.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritem">ITfSystemLangBarItem
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
