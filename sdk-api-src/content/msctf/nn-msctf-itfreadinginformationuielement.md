---
UID: NN:msctf.ITfReadingInformationUIElement
title: ITfReadingInformationUIElement (msctf.h)

description: The ITfCandidateListUIElement interface is implemented by a text service that has a UI for reading information UI at the near caret.
old-location: tsf\itfreadinginformationuielement.htm
tech.root: TSF
ms.assetid: 60f7c6e2-7821-4be6-a1c1-35bacaa60bf4

ms.date: 12/05/2018
ms.keywords: ITfReadingInformationUIElement, ITfReadingInformationUIElement interface [Text Services Framework], ITfReadingInformationUIElement interface [Text Services Framework],described, msctf/ITfReadingInformationUIElement, tsf.itfreadinginformationuielement
ms.topic: interface
f1_keywords: 
 - "msctf/ITfReadingInformationUIElement"
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
 - ITfReadingInformationUIElement
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfReadingInformationUIElement interface


## -description


The <b>ITfCandidateListUIElement</b> interface is implemented by a text service that has a UI for reading information UI at the near caret.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReadingInformationUIElement</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReadingInformationUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReadingInformationUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadinginformationuielement-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Returns the target ITfContext of this reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa382693(v=vs.85)">GetErrorIndex</a>
</td>
<td align="left" width="63%">
Returns the char index where the typing error occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadinginformationuielement-getmaxreadingstringlength">GetMaxReadingStringLength</a>
</td>
<td align="left" width="63%">
Returns the max string count of the reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadinginformationuielement-getstring">GetString</a>
</td>
<td align="left" width="63%">
Returns the string on the reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadinginformationuielement-getupdatedflags">GetUpdatedFlags</a>
</td>
<td align="left" width="63%">
Returns the flag that tells which part of this element was updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreadinginformationuielement-isverticalorderpreferred">IsVerticalOrderPreferred</a>
</td>
<td align="left" width="63%">
Returns if the UI prefers to be shown in vertical order.

</td>
</tr>
</table> 

