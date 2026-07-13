---
UID: NN:ctfutb.ITfSystemLangBarItem
title: ITfSystemLangBarItem (ctfutb.h)
description: The ITfSystemLangBarItem interface is implemented by a system language bar menu and is used by a system language bar extension to modify the icon and/or tooltip string displayed for the menu.
helpviewer_keywords: ["ITfSystemLangBarItem","ITfSystemLangBarItem interface [Text Services Framework]","ITfSystemLangBarItem interface [Text Services Framework]","described","_tsf_itfsystemlangbaritem_ref","ctfutb/ITfSystemLangBarItem","tsf.itfsystemlangbaritem"]
old-location: tsf\itfsystemlangbaritem.htm
tech.root: TSF
ms.assetid: 9b41e787-eb90-4858-8838-8c36c7dce0c1
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItem, ITfSystemLangBarItem interface [Text Services Framework], ITfSystemLangBarItem interface [Text Services Framework],described, _tsf_itfsystemlangbaritem_ref, ctfutb/ITfSystemLangBarItem, tsf.itfsystemlangbaritem
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
 - ITfSystemLangBarItem
 - ctfutb/ITfSystemLangBarItem
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
 - ITfSystemLangBarItem
---

# ITfSystemLangBarItem interface


## -description

The <b>ITfSystemLangBarItem</b> interface is implemented by a system language bar menu and is used by a system language bar extension to modify the icon and/or tooltip string displayed for the menu. The extension can obtain an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object with IID_ITfSystemLangBarItem.

## -inheritance

The <b>ITfSystemLangBarItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSystemLangBarItem</b> also has these types of members:

## -remarks

A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> implementation. The system item should also implement the <b>ITfSystemLangBarItem</b> interface. The system item uses the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink">ITfSystemLangBarItemSink</a> interface to enable the extension to add items.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink">ITfSystemLangBarItemSink</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
