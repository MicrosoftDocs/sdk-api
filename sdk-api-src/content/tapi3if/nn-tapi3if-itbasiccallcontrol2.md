---
UID: NN:tapi3if.ITBasicCallControl2
title: ITBasicCallControl2 (tapi3if.h)
description: The ITBasicCallControl2 interface is an extension of the ITBasicCallControl interface.
helpviewer_keywords: ["ITBasicCallControl2","ITBasicCallControl2 interface [TAPI 2.2]","ITBasicCallControl2 interface [TAPI 2.2]","described","_tapi3_itbasiccallcontrol2","tapi3.itbasiccallcontrol2","tapi3if/ITBasicCallControl2"]
old-location: tapi3\itbasiccallcontrol2.htm
tech.root: tapi3
ms.assetid: fc693221-b7ba-4b33-aed7-59ec92fc9b58
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl2, ITBasicCallControl2 interface [TAPI 2.2], ITBasicCallControl2 interface [TAPI 2.2],described, _tapi3_itbasiccallcontrol2, tapi3.itbasiccallcontrol2, tapi3if/ITBasicCallControl2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl2
 - tapi3if/ITBasicCallControl2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl2
---

# ITBasicCallControl2 interface


## -description

The 
<b>ITBasicCallControl2</b> interface is an extension of the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface. 
<b>ITBasicCallControl2</b> supplies additional methods that allow an application to select a terminal onto a call. The 
<b>ITBasicCallControl2</b> interface is created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicCallControl2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITBasicCallControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITBasicCallControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal">RequestTerminal</a>
</td>
<td align="left" width="63%">
Gets a suitable terminal, given the class, media, and direction required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall">SelectTerminalOnCall</a>
</td>
<td align="left" width="63%">
Selects a terminal onto the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall">UnselectTerminalOnCall</a>
</td>
<td align="left" width="63%">
Unselects a terminal from the call.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>