---
UID: NF:azroles.IAzAuthorizationStore.SetProperty
title: IAzAuthorizationStore::SetProperty
author: windows-sdk-content
description: Sets the specified value to the AzAuthorizationStore object property with the specified property ID.
old-location: security\azauthorizationstore_setproperty.htm
old-project: SecAuthZ
ms.assetid: c71a022f-8244-4263-8ff6-6c2d9562fcd1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_AZSTORE_DOMAIN_TIMEOUT, AZ_PROP_AZSTORE_MAX_SCRIPT_ENGINES, AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AzAuthorizationStore object [Security],SetProperty method, IAzAuthorizationStore interface [Security],SetProperty method, IAzAuthorizationStore.SetProperty, IAzAuthorizationStore::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],AzAuthorizationStore object, SetProperty method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::SetProperty, security.azauthorizationstore_setproperty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	AzAuthorizationStore.SetProperty
-	IAzAuthorizationStore.SetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::SetProperty


## -description


The <b>SetProperty</b> method sets the specified value to the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property  to set. The following table shows the possible values.

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
Also accessed through the <a href="https://msdn.microsoft.com/e512641d-a282-41f6-a7d8-5383ad43cd5b">DomainTimeout</a> property

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
<td width="40%"><a id="AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT"></a><a id="az_prop_azstore_script_engine_timeout"></a><dl>
<dt><b>AZ_PROP_AZSTORE_SCRIPT_ENGINE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/7ac3db2d-11a6-4481-a86d-4b3a1063dee3">ScriptEngineTimeout</a> property

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
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/fdace7a9-4b6b-4698-812d-c53fc3b8f0d8">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a> property

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
</table>
 


### -param varProp [in]

Value to set to the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object property  specified by the <i>lPropId</i> parameter. The following table shows the type of data that must be used depending on the value of the <i>lPropId</i> parameter.

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



You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



