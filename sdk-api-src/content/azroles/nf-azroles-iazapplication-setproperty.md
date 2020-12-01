---
UID: NF:azroles.IAzApplication.SetProperty
title: IAzApplication::SetProperty (azroles.h)
description: Sets the specified value to the IAzApplication object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID","AZ_PROP_APPLICATION_DATA","AZ_PROP_APPLICATION_INTERFACE_CLSID","AZ_PROP_APPLICATION_VERSION","AZ_PROP_APPLY_STORE_SACL","AZ_PROP_DESCRIPTION","AZ_PROP_GENERATE_AUDITS","AZ_PROP_NAME","AzApplication object [Security]","SetProperty method","IAzApplication interface [Security]","SetProperty method","IAzApplication.SetProperty","IAzApplication::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","AzApplication object","SetProperty method [Security]","IAzApplication interface","azroles/IAzApplication::SetProperty","security.iazapplication_setproperty"]
old-location: security\iazapplication_setproperty.htm
tech.root: security
ms.assetid: 077ed5a9-7a38-4477-9fac-1f0b88ab0d33
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID, AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLICATION_INTERFACE_CLSID, AZ_PROP_APPLICATION_VERSION, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AZ_PROP_NAME, AzApplication object [Security],SetProperty method, IAzApplication interface [Security],SetProperty method, IAzApplication.SetProperty, IAzApplication::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],AzApplication object, SetProperty method [Security],IAzApplication interface, azroles/IAzApplication::SetProperty, security.iazapplication_setproperty
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
 - IAzApplication::SetProperty
 - azroles/IAzApplication::SetProperty
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
 - IAzApplication.SetProperty
 - AzApplication.SetProperty
---

# IAzApplication::SetProperty


## -description

The <b>SetProperty</b> method sets the specified value to the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property  to set. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applicationdata">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID"></a><a id="az_prop_application_authz_interface_clsid"></a><dl>
<dt><b>AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_authzinterfaceclsid">AuthzInterfaceClsid</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_VERSION"></a><a id="az_prop_application_version"></a><dl>
<dt><b>AZ_PROP_APPLICATION_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_version">Version</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applystoresacl">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_generateaudits">GenerateAudits</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_name">Name</a> property

</td>
</tr>
</table>

### -param varProp [in]

Value to set to the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property  specified by the <i>lPropId</i> parameter. The type of data that must be used depends on the value of the <i>lPropId</i> parameter.

<table>
<tr>
<th><i>lPropId</i> value</th>
<th>Data type (C++/Visual Basic)</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_INTERFACE_CLSID"></a><a id="az_prop_application_interface_clsid"></a><dl>
<dt><b>AZ_PROP_APPLICATION_INTERFACE_CLSID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_VERSION"></a><a id="az_prop_application_version"></a><dl>
<dt><b>AZ_PROP_APPLICATION_VERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.