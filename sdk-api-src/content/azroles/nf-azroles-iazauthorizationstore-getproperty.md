---
UID: NF:azroles.IAzAuthorizationStore.GetProperty
title: IAzAuthorizationStore::GetProperty (azroles.h)
description: Returns the AzAuthorizationStore object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_APPLY_STORE_SACL","AZ_PROP_AZSTORE_DOMAIN_TIMEOUT","AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES","AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT","AZ_PROP_AZSTORE_TARGET_MACHINE","AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_GENERATE_AUDITS","AZ_PROP_WRITABLE","AzAuthorizationStore object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzAuthorizationStore object","GetProperty method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","GetProperty method","IAzAuthorizationStore.GetProperty","IAzAuthorizationStore::GetProperty","azroles/IAzAuthorizationStore::GetProperty","security.azauthorizationstore_getproperty"]
old-location: security\azauthorizationstore_getproperty.htm
tech.root: security
ms.assetid: 93bd6813-cc46-4f48-b39b-1e67cda562ff
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_AZSTORE_DOMAIN_TIMEOUT, AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES, AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT, AZ_PROP_AZSTORE_TARGET_MACHINE, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AZ_PROP_WRITABLE, AzAuthorizationStore object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzAuthorizationStore object, GetProperty method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],GetProperty method, IAzAuthorizationStore.GetProperty, IAzAuthorizationStore::GetProperty, azroles/IAzAuthorizationStore::GetProperty, security.azauthorizationstore_getproperty
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore::GetProperty
 - azroles/IAzAuthorizationStore::GetProperty
dev_langs:
 - c++
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
---

# IAzAuthorizationStore::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applicationdata">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_DOMAIN_TIMEOUT"></a><a id="az_prop_azstore_domain_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_DOMAIN_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_domaintimeout">DomainTimeout</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT"></a><a id="az_prop_azstore_script_engine_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_scriptenginetimeout">ScriptEngineTimeout</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES"></a><a id="az_prop_azstore_max_script_engines"></a><dl>
<dt><b>AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_maxscriptengines">MaxScriptEngines</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_TARGET_MACHINE"></a><a id="az_prop_azstore_target_machine"></a><dl>
<dt><b>AZ_PROP_AZSTORE_TARGET_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_targetmachine">TargetMachine</a> property

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_generateaudits">GenerateAudits</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applystoresacl">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_writable">Writable</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.