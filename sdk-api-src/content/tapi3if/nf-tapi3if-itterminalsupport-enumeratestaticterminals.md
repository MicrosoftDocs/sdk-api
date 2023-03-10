---
UID: NF:tapi3if.ITTerminalSupport.EnumerateStaticTerminals
title: ITTerminalSupport::EnumerateStaticTerminals (tapi3if.h)
description: The EnumerateStaticTerminals method enumerates the currently available static terminals associated with the address.
helpviewer_keywords: ["EnumerateStaticTerminals","EnumerateStaticTerminals method [TAPI 2.2]","EnumerateStaticTerminals method [TAPI 2.2]","ITTerminalSupport interface","ITTerminalSupport interface [TAPI 2.2]","EnumerateStaticTerminals method","ITTerminalSupport.EnumerateStaticTerminals","ITTerminalSupport::EnumerateStaticTerminals","_tapi3_itterminalsupport_enumeratestaticterminals","tapi3.itterminalsupport_enumeratestaticterminals","tapi3if/ITTerminalSupport::EnumerateStaticTerminals"]
old-location: tapi3\itterminalsupport_enumeratestaticterminals.htm
tech.root: tapi3
ms.assetid: 91fea706-9792-40e1-b812-f7578bc7968b
ms.date: 12/05/2018
ms.keywords: EnumerateStaticTerminals, EnumerateStaticTerminals method [TAPI 2.2], EnumerateStaticTerminals method [TAPI 2.2],ITTerminalSupport interface, ITTerminalSupport interface [TAPI 2.2],EnumerateStaticTerminals method, ITTerminalSupport.EnumerateStaticTerminals, ITTerminalSupport::EnumerateStaticTerminals, _tapi3_itterminalsupport_enumeratestaticterminals, tapi3.itterminalsupport_enumeratestaticterminals, tapi3if/ITTerminalSupport::EnumerateStaticTerminals
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITTerminalSupport::EnumerateStaticTerminals
 - tapi3if/ITTerminalSupport::EnumerateStaticTerminals
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport.EnumerateStaticTerminals
---

# ITTerminalSupport::EnumerateStaticTerminals


## -description

The 
<b>EnumerateStaticTerminals</b> method enumerates the currently available static terminals associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">get_StaticTerminals</a> method.

## -parameters

### -param ppTerminalEnumerator [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> enumerator.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminalEnumerator</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface returned by <b>ITTerminalSupport::EnumerateStaticTerminals</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>