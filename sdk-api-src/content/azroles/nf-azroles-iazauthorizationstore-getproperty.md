---
UID: NF:azroles.IAzAuthorizationStore.GetProperty
title: IAzAuthorizationStore::GetProperty
author: windows-sdk-content
description: Returns the AzAuthorizationStore object property with the specified property ID.
old-location: security\azauthorizationstore_getproperty.htm
tech.root: secauthz
ms.assetid: 93bd6813-cc46-4f48-b39b-1e67cda562ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_AZSTORE_DOMAIN_TIMEOUT, AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES, AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT, AZ_PROP_AZSTORE_TARGET_MACHINE, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AZ_PROP_WRITABLE, AzAuthorizationStore object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzAuthorizationStore object, GetProperty method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],GetProperty method, IAzAuthorizationStore.GetProperty, IAzAuthorizationStore::GetProperty, azroles/IAzAuthorizationStore::GetProperty, security.azauthorizationstore_getproperty
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - AzAuthorizationStore.GetProperty
 - IAzAuthorizationStore.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property  to return. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/79ef0e2f-3178-4310-832c-b0eea06cf1b0">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/21a76185-6bcf-405a-a2c5-5509b51ed16e">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_DOMAIN_TIMEOUT"></a><a id="az_prop_azstore_domain_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_DOMAIN_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/e512641d-a282-41f6-a7d8-5383ad43cd5b">DomainTimeout</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT"></a><a id="az_prop_azstore_script_engine_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/7ac3db2d-11a6-4481-a86d-4b3a1063dee3">ScriptEngineTimeout</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES"></a><a id="az_prop_azstore_max_script_engines"></a><dl>
<dt><b>AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/d18fe030-5177-4516-b4bf-6fea78abea52">MaxScriptEngines</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_TARGET_MACHINE"></a><a id="az_prop_azstore_target_machine"></a><dl>
<dt><b>AZ_PROP_AZSTORE_TARGET_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/60c3c23a-4721-4f0d-8380-e95b6170c804">TargetMachine</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value is <b>TRUE</b> if the current user has permission; otherwise, <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/e9362ae0-488d-4b6b-9a7b-c70fd85042ca">GenerateAudits</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/fdace7a9-4b6b-4698-812d-c53fc3b8f0d8">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/0c896364-739a-456a-97f7-0448711462b3">Writable</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



