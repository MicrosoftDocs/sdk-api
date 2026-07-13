---
UID: NF:tapi3cc.ITAgentHandler.EnumerateACDGroups
title: ITAgentHandler::EnumerateACDGroups (tapi3cc.h)
description: The ITAgentHandler::EnumerateACDGroups method (tapi3cc.h) enumerates ACD groups currently associated with the agent handler.
helpviewer_keywords: ["EnumerateACDGroups","EnumerateACDGroups method [TAPI 2.2]","EnumerateACDGroups method [TAPI 2.2]","ITAgentHandler interface","ITAgentHandler interface [TAPI 2.2]","EnumerateACDGroups method","ITAgentHandler.EnumerateACDGroups","ITAgentHandler::EnumerateACDGroups","_tapi3_itagenthandler_enumerateacdgroups","tapi3.itagenthandler_enumerateacdgroups","tapi3cc/ITAgentHandler::EnumerateACDGroups"]
old-location: tapi3\itagenthandler_enumerateacdgroups.htm
tech.root: tapi3
ms.assetid: a9078166-ff6a-4520-8209-e785bd6e7100
ms.date: 08/10/2022
ms.keywords: EnumerateACDGroups, EnumerateACDGroups method [TAPI 2.2], EnumerateACDGroups method [TAPI 2.2],ITAgentHandler interface, ITAgentHandler interface [TAPI 2.2],EnumerateACDGroups method, ITAgentHandler.EnumerateACDGroups, ITAgentHandler::EnumerateACDGroups, _tapi3_itagenthandler_enumerateacdgroups, tapi3.itagenthandler_enumerateacdgroups, tapi3cc/ITAgentHandler::EnumerateACDGroups
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
 - ITAgentHandler::EnumerateACDGroups
 - tapi3cc/ITAgentHandler::EnumerateACDGroups
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
 - ITAgentHandler.EnumerateACDGroups
---

# ITAgentHandler::EnumerateACDGroups


## -description

The 
<b>EnumerateACDGroups</b> method enumerates ACD groups currently associated with the agent handler. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_acdgroups">get_ACDGroups</a> method. The number of groups returned is based upon replies from the ACD proxy application. Each proxy application will return a list of groups according to its own internal privilege/security decisions.

## -parameters

### -param ppEnumACDGroup [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a> interface.

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
The <i>ppEnumACDGroup</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a> interface returned by <b>ITAgentHandler::EnumerateACDGroups</b>. The application must call <b>Release</b> on the 
<b>IEnumACDGroup</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumacdgroup">IEnumACDGroup</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>
