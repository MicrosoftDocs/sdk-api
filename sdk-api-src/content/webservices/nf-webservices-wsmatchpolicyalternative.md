---
UID: NF:webservices.WsMatchPolicyAlternative
title: WsMatchPolicyAlternative function (webservices.h)
description: Verifies that a Policy Alternative is compatible with the specified Policy Constraint.
helpviewer_keywords: ["WsMatchPolicyAlternative","WsMatchPolicyAlternative function [Web Services for Windows]","webservices/WsMatchPolicyAlternative","wsw.wsmatchpolicyalternative"]
old-location: wsw\wsmatchpolicyalternative.htm
tech.root: wsw
ms.assetid: 6e5f352b-5422-4bba-9525-7850bdddf0a5
ms.date: 12/05/2018
ms.keywords: WsMatchPolicyAlternative, WsMatchPolicyAlternative function [Web Services for Windows], webservices/WsMatchPolicyAlternative, wsw.wsmatchpolicyalternative
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
 - WsMatchPolicyAlternative
 - webservices/WsMatchPolicyAlternative
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
 - WsMatchPolicyAlternative
---

# WsMatchPolicyAlternative function


## -description

Verifies that a Policy Alternative is compatible
                with the specified Policy Constraint.  If the alternative is compatible the constraint structures are populated with Policy information.
            <div class="alert"><b>Note</b>  See Remarks on this page for information on the constraint structures.</div>
<div> </div>

## -parameters

### -param policy [in]

A pointer to a  <a href="/windows/desktop/wsw/ws-policy">WS_POLICY</a> object  containing the alternative.
                
<div class="alert"><b>Note</b>  Each <a href="/windows/desktop/api/webservices/ns-webservices-ws_metadata_endpoint">WS_METADATA_ENDPOINT</a> that is returned from <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmetadataendpoints">WsGetMetadataEndpoints</a> contains a policy object.
</div>
<div> </div>

### -param alternativeIndex [in]

Specifies the zero-based index that identifies the alternative to use within the policy object. The number of alternatives present in the policy object can be obtained using <a href="/windows/desktop/api/webservices/nf-webservices-wsgetpolicyalternativecount">WsGetPolicyAlternativeCount</a>.

### -param policyConstraints [in]

A pointer to the constraints that specify policies to match along with the fields to populate if the function returns NOERROR.
                

<div class="alert"><b>Note</b>  If a property constraint is not specified the default constraint value for that particular property is used.

See <a href="/windows/desktop/api/webservices/ns-webservices-ws_policy_constraints">WS_POLICY_CONSTRAINTS</a> for more information.</div>
<div> </div>

### -param matchRequired [in]

Indicates whether a match is required or not.  

<div class="alert"><b>Note</b>  If the value is <b>FALSE</b> a match is not required, and in conjunction with a non-matching policy alternative, the function returns S_FALSE.

If the value of this parameter is <b>TRUE</b> a match is required,  and if the policy does not match, the function returns an error.
</div>
<div> </div>

### -param heap [in]

A pointer to a <a href="/windows/desktop/wsw/heap">Heap</a> object used to store any data requiring allocation beyond the specified constraint. 
<div class="alert"><b>Note</b>  For example pointer types within the constraint "out" fields is allocated using this Heap.
</div>
<div> </div>

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
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The policy alternative does not meet the specified constraints and matchRequired was set to <b>TRUE</b>.
                

The policy or other metadata was in an invalid format.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The policy alternative does not meet the specified constraints and matchRequired was set to <b>FALSE</b>.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The policy alternative meets the specific constraints.  The <b>out</b> fields of the constraints structures have been filled with values from the policy.
                

</td>
</tr>
</table>

## -remarks

Each of these data types contain a struct field called "out".         

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_channel_property_constraint">WS_CHANNEL_PROPERTY_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_property_constraint">WS_SECURITY_PROPERTY_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_property_constraint">WS_SECURITY_BINDING_PROPERTY_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_ssl_transport_security_binding_constraint">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
The content of the <b>out</b> field of these structures is populated by this function if the call returns NOERROR.
            

<div class="alert"><b>Note</b>  If the function call fails the content <b>out</b> may have been partially set and only some allocations may have been made from the specified heap object. The content of the <b>out</b> field must not be examined unless the function returns NOERROR.
            
<p class="note">The policy object may delay some processing until this function is called.  If the processing fails the policy object is set to  <b>WS_POLICY_STATE_FAULTED</b>.
            

</div>
<div> </div>