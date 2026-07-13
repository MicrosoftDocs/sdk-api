---
UID: NF:tapi3cc.ITAgentHandler.EnumerateUsableAddresses
title: ITAgentHandler::EnumerateUsableAddresses (tapi3cc.h)
description: The ITAgentHandler::EnumerateUsableAddresses method (tapi3cc.h) enumerates addresses available for receiving ACD calls on this agent handler.
helpviewer_keywords: ["EnumerateUsableAddresses","EnumerateUsableAddresses method [TAPI 2.2]","EnumerateUsableAddresses method [TAPI 2.2]","ITAgentHandler interface","ITAgentHandler interface [TAPI 2.2]","EnumerateUsableAddresses method","ITAgentHandler.EnumerateUsableAddresses","ITAgentHandler::EnumerateUsableAddresses","_tapi3_itagenthandler_enumerateusableaddresses","tapi3.itagenthandler_enumerateusableaddresses","tapi3cc/ITAgentHandler::EnumerateUsableAddresses"]
old-location: tapi3\itagenthandler_enumerateusableaddresses.htm
tech.root: tapi3
ms.assetid: 9821b073-c64b-4f2b-b771-6bf027f9aa70
ms.date: 08/10/2022
ms.keywords: EnumerateUsableAddresses, EnumerateUsableAddresses method [TAPI 2.2], EnumerateUsableAddresses method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],EnumerateUsableAddresses method, ITAgentHandler.EnumerateUsableAddresses, ITAgentHandler::EnumerateUsableAddresses, _tapi3_itagenthandler_enumerateusableaddresses, tapi3.itagenthandler_enumerateusableaddresses, tapi3cc/ITAgentHandler::EnumerateUsableAddresses
req.header: tapi3cc.h
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
 - ITAgentHandler::EnumerateUsableAddresses
 - tapi3cc/ITAgentHandler::EnumerateUsableAddresses
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
 - ITAgentHandler.EnumerateUsableAddresses
---

# ITAgentHandler::EnumerateUsableAddresses


## -description

The 
<b>EnumerateUsableAddresses</b> method enumerates addresses available for receiving ACD calls on this agent handler. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_usableaddresses">get_UsableAddresses</a> method.

## -parameters

### -param ppEnumAddress [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress">IEnumAddress</a> interface returned by <b>ITAgentHandler::EnumerateUsableAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>
