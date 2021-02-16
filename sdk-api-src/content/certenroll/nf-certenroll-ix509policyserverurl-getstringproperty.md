---
UID: NF:certenroll.IX509PolicyServerUrl.GetStringProperty
title: IX509PolicyServerUrl::GetStringProperty (certenroll.h)
description: Retrieves the certificate enrollment policy (CEP) server ID or the display name of the CEP server.
helpviewer_keywords: ["GetStringProperty","GetStringProperty method [Security]","GetStringProperty method [Security]","IX509PolicyServerUrl interface","IX509PolicyServerUrl interface [Security]","GetStringProperty method","IX509PolicyServerUrl.GetStringProperty","IX509PolicyServerUrl::GetStringProperty","PsFriendlyName","PsPolicyID","certenroll/IX509PolicyServerUrl::GetStringProperty","security.ix509policyserverurl_getstringproperty"]
old-location: security\ix509policyserverurl_getstringproperty.htm
tech.root: security
ms.assetid: 1a163774-2e32-48f7-9aa1-cbfa0ec7a943
ms.date: 12/05/2018
ms.keywords: GetStringProperty, GetStringProperty method [Security], GetStringProperty method [Security],IX509PolicyServerUrl interface, IX509PolicyServerUrl interface [Security],GetStringProperty method, IX509PolicyServerUrl.GetStringProperty, IX509PolicyServerUrl::GetStringProperty, PsFriendlyName, PsPolicyID, certenroll/IX509PolicyServerUrl::GetStringProperty, security.ix509policyserverurl_getstringproperty
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
 - IX509PolicyServerUrl::GetStringProperty
 - certenroll/IX509PolicyServerUrl::GetStringProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509PolicyServerUrl.GetStringProperty
---

# IX509PolicyServerUrl::GetStringProperty


## -description

The <b>GetStringProperty</b> method retrieves the certificate enrollment policy (CEP) server ID or the display name of the CEP server.

## -parameters

### -param propertyId [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-policyserverurlpropertyid">PolicyServerUrlPropertyID</a> value that specifies the string to retrieve. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsPolicyID"></a><a id="pspolicyid"></a><a id="PSPOLICYID"></a><dl>
<dt><b>PsPolicyID</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an ID string for the policy server.

</td>
</tr>
<tr>
<td width="40%"><a id="PsFriendlyName"></a><a id="psfriendlyname"></a><a id="PSFRIENDLYNAME"></a><dl>
<dt><b>PsFriendlyName</b></dt>
</dl>
</td>
<td width="60%">
Retrieve a display name for the policy server.

</td>
</tr>
</table>

### -param ppValue [out, retval]

Pointer to a <b>BSTR</b> variable that receives the property value.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The property value cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>propertyId</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the return value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a>