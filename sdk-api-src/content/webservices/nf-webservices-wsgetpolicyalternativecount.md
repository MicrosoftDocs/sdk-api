---
UID: NF:webservices.WsGetPolicyAlternativeCount
title: WsGetPolicyAlternativeCount function (webservices.h)
description: Retrieves the number of alternatives available in the policy object. The alternative count can be used to loop through each alternative using WsMatchPolicyAlternative.
helpviewer_keywords: ["WsGetPolicyAlternativeCount","WsGetPolicyAlternativeCount function [Web Services for Windows]","webservices/WsGetPolicyAlternativeCount","wsw.wsgetpolicyalternativecount"]
old-location: wsw\wsgetpolicyalternativecount.htm
tech.root: wsw
ms.assetid: 2d3ac397-07a0-45c4-84b4-0f4806a324bc
ms.date: 12/05/2018
ms.keywords: WsGetPolicyAlternativeCount, WsGetPolicyAlternativeCount function [Web Services for Windows], webservices/WsGetPolicyAlternativeCount, wsw.wsgetpolicyalternativecount
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsGetPolicyAlternativeCount
 - webservices/WsGetPolicyAlternativeCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetPolicyAlternativeCount
---

# WsGetPolicyAlternativeCount function


## -description

Retrieves the number of alternatives available in the policy object.
            The alternative count can be used to loop through each alternative using
                <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a>.
            


<div class="alert"><b>Note</b>  The policy object may delay some processing until this function is called.  If the
                processing fails, then the policy object will be set to
                <b>WS_POLICY_STATE_FAULTED</b> state.
            </div><div> </div>

## -parameters

### -param policy [in]

A pointer to the <a href="/windows/desktop/wsw/ws-policy">WS_POLICY</a> object from which to count alternatives.

### -param count [out]

A pointer to the number value of alternatives.  This may be 0.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property id was not supported for this object or the specified buffer was not large enough for the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

Note that each alternative is not guaranteed to be unique within the policy
                (there may be duplicates).