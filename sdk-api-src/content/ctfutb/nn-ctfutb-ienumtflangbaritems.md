---
UID: NN:ctfutb.IEnumTfLangBarItems
title: IEnumTfLangBarItems (ctfutb.h)
description: The IEnumTfLangBarItems interface is implemented by the TSF manager to provide an enumeration of langauge bar item objects.
helpviewer_keywords: ["IEnumTfLangBarItems","IEnumTfLangBarItems interface [Text Services Framework]","IEnumTfLangBarItems interface [Text Services Framework]","described","_tsf_ienumtflangbaritems_ref","ctfutb/IEnumTfLangBarItems","tsf.ienumtflangbaritems"]
old-location: tsf\ienumtflangbaritems.htm
tech.root: TSF
ms.assetid: a3988c0f-db2d-4841-8098-f1dc133cb60a
ms.date: 12/05/2018
ms.keywords: IEnumTfLangBarItems, IEnumTfLangBarItems interface [Text Services Framework], IEnumTfLangBarItems interface [Text Services Framework],described, _tsf_ienumtflangbaritems_ref, ctfutb/IEnumTfLangBarItems, tsf.ienumtflangbaritems
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
 - IEnumTfLangBarItems
 - ctfutb/IEnumTfLangBarItems
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
 - IEnumTfLangBarItems
---

# IEnumTfLangBarItems interface


## -description

The <b>IEnumTfLangBarItems</b> interface is implemented by the TSF manager to provide an enumeration of langauge bar item objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfLangBarItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfLangBarItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfLangBarItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ctfutb/nf-ctfutb-ienumtflangbaritems-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ctfutb/nf-ctfutb-ienumtflangbaritems-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ctfutb/nf-ctfutb-ienumtflangbaritems-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ctfutb/nf-ctfutb-ienumtflangbaritems-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table>