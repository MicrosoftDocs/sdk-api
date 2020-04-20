---
UID: NN:msctf.IEnumTfUIElements
title: IEnumTfUIElements (msctf.h)
description: The IEnumTfUIElements interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by ITfUIElementMgr::EnumUIElements and enumerates the registered UI elements.helpviewer_keywords: ["IEnumTfUIElements","IEnumTfUIElements interface [Text Services Framework]","IEnumTfUIElements interface [Text Services Framework]","described","_tsf_ienumtfuielements_ref","msctf/IEnumTfUIElements","tsf.ienumtfuielements"]
old-location: tsf\ienumtfuielements.htm
tech.root: TSF
ms.assetid: 5ee3d89c-0761-4d4b-9fd9-6b9de7ceb077
ms.date: 12/05/2018
ms.keywords: IEnumTfUIElements, IEnumTfUIElements interface [Text Services Framework], IEnumTfUIElements interface [Text Services Framework],described, _tsf_ienumtfuielements_ref, msctf/IEnumTfUIElements, tsf.ienumtfuielements
f1_keywords:
- msctf/IEnumTfUIElements
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
- IEnumTfUIElements
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfUIElements interface


## -description


The <b>IEnumTfUIElements</b> interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-enumuielements">ITfUIElementMgr::EnumUIElements</a>  and enumerates the registered UI elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfUIElements</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfUIElements</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfUIElements</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfuielements-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfuielements-next">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfuielements-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfuielements-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

