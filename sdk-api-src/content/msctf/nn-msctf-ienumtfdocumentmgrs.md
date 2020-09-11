---
UID: NN:msctf.IEnumTfDocumentMgrs
title: IEnumTfDocumentMgrs (msctf.h)
description: The IEnumTfDocumentMgrs interface is implemented by the TSF manager to provide an enumeration of document manager objects.
helpviewer_keywords: ["IEnumTfDocumentMgrs","IEnumTfDocumentMgrs interface [Text Services Framework]","IEnumTfDocumentMgrs interface [Text Services Framework]","described","_tsf_ienumtfdocumentmgrs_ref","msctf/IEnumTfDocumentMgrs","tsf.ienumtfdocumentmgrs"]
old-location: tsf\ienumtfdocumentmgrs.htm
tech.root: TSF
ms.assetid: 5b276752-715b-4426-ad37-8658bae4c1a6
ms.date: 12/05/2018
ms.keywords: IEnumTfDocumentMgrs, IEnumTfDocumentMgrs interface [Text Services Framework], IEnumTfDocumentMgrs interface [Text Services Framework],described, _tsf_ienumtfdocumentmgrs_ref, msctf/IEnumTfDocumentMgrs, tsf.ienumtfdocumentmgrs
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
 - IEnumTfDocumentMgrs
 - msctf/IEnumTfDocumentMgrs
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
 - IEnumTfDocumentMgrs
---

# IEnumTfDocumentMgrs interface


## -description

The **IEnumTfDocumentMgrs** interface is implemented by the TSF manager to provide an enumeration of document manager objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfDocumentMgrs</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfDocumentMgrs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfDocumentMgrs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdocumentmgrs-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdocumentmgrs-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdocumentmgrs-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfdocumentmgrs-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table>

