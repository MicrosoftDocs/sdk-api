---
UID: NN:tapi3if.IEnumTerminal
title: IEnumTerminal (tapi3if.h)
description: The IEnumTerminal interface provides COM-standard enumeration methods for the ITTerminal interface.
helpviewer_keywords: ["IEnumTerminal","IEnumTerminal interface [TAPI 2.2]","IEnumTerminal interface [TAPI 2.2]","described","_tapi3_ienumterminal","tapi3.ienumterminal","tapi3if/IEnumTerminal"]
old-location: tapi3\ienumterminal.htm
tech.root: Tapi
ms.assetid: a364e466-1d10-402f-935d-ff2713522fed
ms.date: 12/05/2018
ms.keywords: IEnumTerminal, IEnumTerminal interface [TAPI 2.2], IEnumTerminal interface [TAPI 2.2],described, _tapi3_ienumterminal, tapi3.ienumterminal, tapi3if/IEnumTerminal
f1_keywords:
- tapi3if/IEnumTerminal
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- IEnumTerminal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumTerminal interface


## -description


The 
<b>IEnumTerminal</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface. The following methods return a pointer to 
<b>IEnumTerminal</b>:<dl>
<dd>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-enumerateterminals">ITStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-enumerateterminals">ITSubStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a>
</dd>
</dl>


The 
<b>IEnumTerminal</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTerminal</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTerminal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumterminal-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumterminal-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumterminal-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumterminal-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>
 

 

