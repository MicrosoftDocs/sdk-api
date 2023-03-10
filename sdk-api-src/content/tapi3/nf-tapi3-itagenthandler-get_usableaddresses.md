---
UID: NF:tapi3.ITAgentHandler.get_UsableAddresses
title: ITAgentHandler::get_UsableAddresses (tapi3.h)
description: The get_UsableAddresses method (tapi3.h) creates a collection of addresses available for receiving ACD calls on this agent handler.
helpviewer_keywords: ["ITAgentHandler interface [TAPI 2.2]","get_UsableAddresses method","ITAgentHandler.get_UsableAddresses","ITAgentHandler::get_UsableAddresses","_tapi3_itagenthandler_get_usableaddresses","get_UsableAddresses","get_UsableAddresses method [TAPI 2.2]","get_UsableAddresses method [TAPI 2.2]","ITAgentHandler interface","tapi3.itagenthandler_get_usableaddresses","tapi3cc/ITAgentHandler::get_UsableAddresses"]
old-location: tapi3\itagenthandler_get_usableaddresses.htm
tech.root: tapi3
ms.assetid: ee457b5c-e505-489c-93dc-8bdfb87c7afe
ms.date: 08/09/2022
ms.keywords: ITAgentHandler interface [TAPI 2.2],get_UsableAddresses method, ITAgentHandler.get_UsableAddresses, ITAgentHandler::get_UsableAddresses, _tapi3_itagenthandler_get_usableaddresses, get_UsableAddresses, get_UsableAddresses method [TAPI 2.2], get_UsableAddresses method [TAPI 2.2],ITAgentHandler interface, tapi3.itagenthandler_get_usableaddresses, tapi3cc/ITAgentHandler::get_UsableAddresses
req.header: tapi3.h
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
 - ITAgentHandler::get_UsableAddresses
 - tapi3/ITAgentHandler::get_UsableAddresses
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
 - ITAgentHandler.get_UsableAddresses
---

# ITAgentHandler::get_UsableAddresses


## -description

The 
<b>get_UsableAddresses</b> method creates a collection of addresses available for receiving ACD calls on this agent handler. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateusableaddresses">EnumerateUsableAddresses</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface pointers (address objects).

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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITAgentHandler::get_UsableAddresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateusableaddresses">EnumerateUsableAddresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>
