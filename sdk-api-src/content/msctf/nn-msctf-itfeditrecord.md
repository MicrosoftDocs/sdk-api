---
UID: NN:msctf.ITfEditRecord
title: ITfEditRecord (msctf.h)
description: The ITfEditRecord interface is implemented by the TSF manager and is used by a text edit sink to determine what was changed during an edit session.
helpviewer_keywords: ["ITfEditRecord","ITfEditRecord interface [Text Services Framework]","ITfEditRecord interface [Text Services Framework]","described","_tsf_itfeditrecord_ref","msctf/ITfEditRecord","tsf.itfeditrecord"]
old-location: tsf\itfeditrecord.htm
tech.root: TSF
ms.assetid: 2106cd97-9e1f-4d7c-a7a4-55676cf8923b
ms.date: 12/05/2018
ms.keywords: ITfEditRecord, ITfEditRecord interface [Text Services Framework], ITfEditRecord interface [Text Services Framework],described, _tsf_itfeditrecord_ref, msctf/ITfEditRecord, tsf.itfeditrecord
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
 - ITfEditRecord
 - msctf/ITfEditRecord
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
 - ITfEditRecord
---

# ITfEditRecord interface


## -description

The <b>ITfEditRecord</b> interface is implemented by the TSF manager and is used by a text edit sink to determine what was changed during an edit session. An instance of this interface is passed to the text edit sink when the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> method is called.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfEditRecord</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfEditRecord</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfEditRecord</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditrecord-getselectionstatus">GetSelectionStatus</a>
</td>
<td align="left" width="63%">
Determines if the selection has changed during the edit session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates">GetTextAndPropertyUpdates</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains a collection of range objects that cover the specified properties and/or text that changed during the edit session.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

