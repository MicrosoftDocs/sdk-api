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

The <b>ITfSystemLangBarItemSink</b> interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu. The extension obtains an instance of this interface by calling QueryInterface on the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object with IID_ITfSystemLangBarItemSink. It can then pass the object to the host by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemLangBarItemSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSystemLangBarItemSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSystemLangBarItemSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu">InitMenu</a>
</td>
<td align="left" width="63%">
Called to allow a system language bar item extension to add items to a system language bar menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the system menu added by the system language bar menu extension.

</td>
</tr>
</table>

## -remarks

A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <b>ITfSource::AdviseSink</b> implementation. The system item should also implement the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritem">ITfSystemLangBarItem</a> interface. The system item uses the <b>ITfSystemLangBarItemSink</b> interface to allow the extension to add its items.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritem">ITfSystemLangBarItem
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

