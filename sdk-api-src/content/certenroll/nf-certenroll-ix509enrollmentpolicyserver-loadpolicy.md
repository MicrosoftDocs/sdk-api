---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IX509EnrollmentPolicyServer::LoadPolicy


## -description


The <b>LoadPolicy</b> method retrieves policy information from the certificate enrollment policy (CEP) server.


## -parameters




### -param option [in]

A value of the <a href="https://msdn.microsoft.com/94adcffd-b4fe-4bd9-912c-9e8d5e5fdb5b">X509EnrollmentPolicyLoadOption</a> enumeration that specifies how to retrieve policy from the policy server. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LoadOptionDefault"></a><a id="loadoptiondefault"></a><a id="LOADOPTIONDEFAULT"></a><dl>
<dt><b>LoadOptionDefault</b></dt>
</dl>
</td>
<td width="60%">
Reload if the cache has expired.

</td>
</tr>
<tr>
<td width="40%"><a id="LoadOptionCacheOnly"></a><a id="loadoptioncacheonly"></a><a id="LOADOPTIONCACHEONLY"></a><dl>
<dt><b>LoadOptionCacheOnly</b></dt>
</dl>
</td>
<td width="60%">
Always load from the cache even if it has expired. This option is not currently supported.

</td>
</tr>
<tr>
<td width="40%"><a id="LoadOptionReload"></a><a id="loadoptionreload"></a><a id="LOADOPTIONRELOAD"></a><dl>
<dt><b>LoadOptionReload</b></dt>
</dl>
</td>
<td width="60%">
Always reload.

</td>
</tr>
<tr>
<td width="40%"><a id="LoadOptionRegisterForADChanges"></a><a id="loadoptionregisterforadchanges"></a><a id="LOADOPTIONREGISTERFORADCHANGES"></a><dl>
<dt><b>LoadOptionRegisterForADChanges</b></dt>
</dl>
</td>
<td width="60%">
Registers a thread to update a sequence number if there are changes to the template or the certification authority container. This value applies only to an Active Directory policy server.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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
The load option requested in the <i>option</i> parameter does not match any supported by the CEP server or you specified LoadOptionCacheOnly in the <i>option</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
There was a problem with the lightweight directory access protocol (LDAP) used to locate the CEP server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

