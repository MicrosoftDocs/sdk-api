---
UID: NN:msctf.ITfUIElement
title: ITfUIElement (msctf.h)
description: The ITfUIElement interface is a base interface of the UIElement object and is implemented by a text service.
old-location: tsf\itfuielement.htm
tech.root: TSF
ms.assetid: 651c3ca1-5e5b-4978-80d2-2183bd158610
ms.date: 12/05/2018
ms.keywords: ITfUIElement, ITfUIElement interface [Text Services Framework], ITfUIElement interface [Text Services Framework],described, _tsf_itfuielement_ref, msctf/ITfUIElement, tsf.itfuielement
ms.topic: interface
f1_keywords:
- msctf/ITfUIElement
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
- ITfUIElement
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfUIElement interface


## -description


The <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElement</a> interface is a base interface of the UIElement object and is implemented by a text service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfUIElement</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielement-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielement-getguid">GetGUID</a>
</td>
<td align="left" width="63%">
Get the unique id of this UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielement-isshown">IsShown</a>
</td>
<td align="left" width="63%">
Return true if the UI is currently shown by a text service; otherwise false.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielement-show">Show</a>
</td>
<td align="left" width="63%">
Shows the text service's UI of this UI element.

</td>
</tr>
</table> 


## -remarks



A text service may implement some other UIElement interface such as <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a> in the same object that can be obtained by QI. A text service may implement only the <b>ITfUIElement</b> interface to a UI object that does not have to be drawn by the application but the show status can be controlled by the application. A text service that is categorized by GUID_TFCAT_TIPCAP_UIELEMENTENABLED needs to implement ITfUIElement for any UI object.



