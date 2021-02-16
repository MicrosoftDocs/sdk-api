---
UID: NF:azroles.IAzScope.GetProperty
title: IAzScope::GetProperty (azroles.h)
description: Returns the IAzScope object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_NAME","AZ_PROP_POLICY_ADMINS","AZ_PROP_POLICY_ADMINS_NAME","AZ_PROP_POLICY_READERS","AZ_PROP_POLICY_READERS_NAME","AZ_PROP_SCOPE_BIZRULES_WRITABLE","AZ_PROP_SCOPE_CAN_BE_DELEGATED","AZ_PROP_WRITABLE","AzScope object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzScope object","GetProperty method [Security]","IAzScope interface","IAzScope interface [Security]","GetProperty method","IAzScope.GetProperty","IAzScope::GetProperty","azroles/IAzScope::GetProperty","security.iazscope_getproperty"]
old-location: security\iazscope_getproperty.htm
tech.root: security
ms.assetid: c3b5b526-5662-4971-8ba2-663e4b2c36ff
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AZ_PROP_SCOPE_BIZRULES_WRITABLE, AZ_PROP_SCOPE_CAN_BE_DELEGATED, AZ_PROP_WRITABLE, AzScope object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzScope object, GetProperty method [Security],IAzScope interface, IAzScope interface [Security],GetProperty method, IAzScope.GetProperty, IAzScope::GetProperty, azroles/IAzScope::GetProperty, security.iazscope_getproperty
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
 - IAzScope::GetProperty
 - azroles/IAzScope::GetProperty
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
 - IAzScope.GetProperty
 - AzScope.GetProperty
---

# IAzScope::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_applicationdata">ApplicationData</a> property

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
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_name">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS"></a><a id="az_prop_policy_admins"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyadministrators">PolicyAdministrators</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyadministratorsname">PolicyAdministratorsName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyreaders">PolicyReaders</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyreadersname">PolicyReadersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_SCOPE_BIZRULES_WRITABLE"></a><a id="az_prop_scope_bizrules_writable"></a><dl>
<dt><b>AZ_PROP_SCOPE_BIZRULES_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_bizruleswritable">BizrulesWritable</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_SCOPE_CAN_BE_DELEGATED"></a><a id="az_prop_scope_can_be_delegated"></a><dl>
<dt><b>AZ_PROP_SCOPE_CAN_BE_DELEGATED</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_canbedelegated">CanBeDelegated</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_writable">Writable</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object property.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.