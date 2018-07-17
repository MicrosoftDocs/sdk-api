---
UID: NF:certenroll.IX509EnrollmentPolicyServer.LoadPolicy
title: IX509EnrollmentPolicyServer::LoadPolicy
author: windows-sdk-content
description: Retrieves policy information from the certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_loadpolicy.htm
old-project: seccertenroll
ms.assetid: 5b617c6e-91bc-4a22-acd6-41083102850a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IX509EnrollmentPolicyServer interface [Security],LoadPolicy method, IX509EnrollmentPolicyServer.LoadPolicy, IX509EnrollmentPolicyServer::LoadPolicy, LoadOptionCacheOnly, LoadOptionDefault, LoadOptionRegisterForADChanges, LoadOptionReload, LoadPolicy, LoadPolicy method [Security], LoadPolicy method [Security],IX509EnrollmentPolicyServer interface, certenroll/IX509EnrollmentPolicyServer::LoadPolicy, security.ix509enrollmentpolicyserver_loadpolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.LoadPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

