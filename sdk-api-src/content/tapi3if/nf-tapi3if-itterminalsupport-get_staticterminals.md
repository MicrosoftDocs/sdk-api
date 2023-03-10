---
UID: NF:tapi3if.ITTerminalSupport.get_StaticTerminals
title: ITTerminalSupport::get_StaticTerminals (tapi3if.h)
description: The get_StaticTerminals method creates a collection of currently available static terminals.
helpviewer_keywords: ["ITTerminalSupport interface [TAPI 2.2]","get_StaticTerminals method","ITTerminalSupport.get_StaticTerminals","ITTerminalSupport::get_StaticTerminals","_tapi3_itterminalsupport_get_staticterminals","get_StaticTerminals","get_StaticTerminals method [TAPI 2.2]","get_StaticTerminals method [TAPI 2.2]","ITTerminalSupport interface","tapi3.itterminalsupport_get_staticterminals","tapi3if/ITTerminalSupport::get_StaticTerminals"]
old-location: tapi3\itterminalsupport_get_staticterminals.htm
tech.root: tapi3
ms.assetid: f4cdd3f5-ca8c-4660-b37c-c38779a516dd
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport interface [TAPI 2.2],get_StaticTerminals method, ITTerminalSupport.get_StaticTerminals, ITTerminalSupport::get_StaticTerminals, _tapi3_itterminalsupport_get_staticterminals, get_StaticTerminals, get_StaticTerminals method [TAPI 2.2], get_StaticTerminals method [TAPI 2.2],ITTerminalSupport interface, tapi3.itterminalsupport_get_staticterminals, tapi3if/ITTerminalSupport::get_StaticTerminals
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
 - ITTerminalSupport::get_StaticTerminals
 - tapi3if/ITTerminalSupport::get_StaticTerminals
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
 - ITTerminalSupport.get_StaticTerminals
---

# ITTerminalSupport::get_StaticTerminals


## -description

The 
<b>get_StaticTerminals</b> method creates a collection of currently available static terminals. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">EnumerateStaticTerminals</a> method.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b>, which TAPI will fill in with an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointers.

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
The <i>pVariant</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITTerminalSupport::get_StaticTerminals</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>