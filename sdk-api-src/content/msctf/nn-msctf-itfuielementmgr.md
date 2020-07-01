---
UID: NN:msctf.ITfUIElementMgr
title: ITfUIElementMgr (msctf.h)
description: The ITfUIElementMgr interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.
helpviewer_keywords: ["ITfUIElementMgr","ITfUIElementMgr interface [Text Services Framework]","ITfUIElementMgr interface [Text Services Framework]","described","_tsf_itfuielementmgr_ref","msctf/ITfUIElementMgr","tsf.itfuielementmgr"]
old-location: tsf\itfuielementmgr.htm
tech.root: TSF
ms.assetid: 7b4d3f4e-bf30-45c6-8709-88b71b25d333
ms.date: 12/05/2018
ms.keywords: ITfUIElementMgr, ITfUIElementMgr interface [Text Services Framework], ITfUIElementMgr interface [Text Services Framework],described, _tsf_itfuielementmgr_ref, msctf/ITfUIElementMgr, tsf.itfuielementmgr
f1_keywords:
- msctf/ITfUIElementMgr
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.h
api_name:
- ITfUIElementMgr
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfUIElementMgr interface


## -description


The <b>ITfUIElementMgr</b> interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfUIElementMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfUIElementMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfUIElementMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-beginuielement">BeginUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method before showing UI. It returns if the text service’s UI should be shown or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-enduielement">EndUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method when the element of UI is hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-enumuielements">EnumUIElements</a>
</td>
<td align="left" width="63%">
Return IEnumTfUIElements interface poinssster to enumerate the ITfUIElement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-getuielement">GetUIElement</a>
</td>
<td align="left" width="63%">
Get ITfUIElement interface of the element id.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-updateuielement">UpdateUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method when the element of UI must be updated.

</td>
</tr>
</table> 


## -remarks



A text service that supports UIElement must call <b>ITfUIElementMgr</b> whenever the UI is shown, updated or hidden. Then the application can control the visibility of the UI.



