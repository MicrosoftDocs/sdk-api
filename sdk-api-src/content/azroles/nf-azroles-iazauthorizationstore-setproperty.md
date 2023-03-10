---
UID: NF:azroles.IAzAuthorizationStore.SetProperty
title: IAzAuthorizationStore::SetProperty (azroles.h)
description: Sets the specified value to the AzAuthorizationStore object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_APPLY_STORE_SACL","AZ_PROP_AZSTORE_DOMAIN_TIMEOUT","AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES","AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT","AZ_PROP_DESCRIPTION","AZ_PROP_GENERATE_AUDITS","AzAuthorizationStore object [Security]","SetProperty method","IAzAuthorizationStore interface [Security]","SetProperty method","IAzAuthorizationStore.SetProperty","IAzAuthorizationStore::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","AzAuthorizationStore object","SetProperty method [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::SetProperty","security.azauthorizationstore_setproperty"]
old-location: security\azauthorizationstore_setproperty.htm
tech.root: security
ms.assetid: c71a022f-8244-4263-8ff6-6c2d9562fcd1
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_AZSTORE_DOMAIN_TIMEOUT, AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES, AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AzAuthorizationStore object [Security],SetProperty method, IAzAuthorizationStore interface [Security],SetProperty method, IAzAuthorizationStore.SetProperty, IAzAuthorizationStore::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],AzAuthorizationStore object, SetProperty method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::SetProperty, security.azauthorizationstore_setproperty
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
 - IAzAuthorizationStore::SetProperty
 - azroles/IAzAuthorizationStore::SetProperty
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
 - AzAuthorizationStore.SetProperty
 - IAzAuthorizationStore.SetProperty
---

# IAzAuthorizationStore::SetProperty


## -description

The <b>SetProperty</b> method sets the specified value to the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property  to set. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<td width="40%"><a id="AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES"></a><a id="az_prop_azstore_max_script_engines"></a><dl>
<dt><b>AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_maxscriptengines">MaxScriptEngines</a> property

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
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_applicationdata">ApplicationData</a> property

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
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_description">Description</a> property

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
</table>

### -param varProp [in]

Value to set to the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object property  specified by the <i>lPropId</i> parameter. The following table shows the type of data that must be used depending on the value of the <i>lPropId</i> parameter.

<table>
<tr>
<th><i>lPropId</i> value</th>
<th>Data type</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_DOMAIN_TIMEOUT"></a><a id="az_prop_azstore_domain_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_DOMAIN_TIMEOUT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>LONG</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES"></a><a id="az_prop_azstore_max_script_engines"></a><dl>
<dt><b>AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>LONG</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT"></a><a id="az_prop_azstore_script_engine_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>LONG</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BOOL</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BOOL</b>

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns <b>S_OK</b>.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.