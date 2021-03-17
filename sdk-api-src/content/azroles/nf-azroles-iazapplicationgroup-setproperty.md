---
UID: NF:azroles.IAzApplicationGroup.SetProperty
title: IAzApplicationGroup::SetProperty (azroles.h)
description: Sets the specified value to the IAzApplicationGroup object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_DESCRIPTION","AZ_PROP_GROUP_LDAP_QUERY","AZ_PROP_GROUP_TYPE","AZ_PROP_NAME","AzApplicationGroup object [Security]","SetProperty method","IAzApplicationGroup interface [Security]","SetProperty method","IAzApplicationGroup.SetProperty","IAzApplicationGroup::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","AzApplicationGroup object","SetProperty method [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::SetProperty","security.iazapplicationgroup_setproperty"]
old-location: security\iazapplicationgroup_setproperty.htm
tech.root: security
ms.assetid: c1af01f2-bd86-4404-a281-2024777dafaa
ms.date: 12/05/2018
ms.keywords: AZ_PROP_DESCRIPTION, AZ_PROP_GROUP_LDAP_QUERY, AZ_PROP_GROUP_TYPE, AZ_PROP_NAME, AzApplicationGroup object [Security],SetProperty method, IAzApplicationGroup interface [Security],SetProperty method, IAzApplicationGroup.SetProperty, IAzApplicationGroup::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],AzApplicationGroup object, SetProperty method [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::SetProperty, security.iazapplicationgroup_setproperty
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
 - IAzApplicationGroup::SetProperty
 - azroles/IAzApplicationGroup::SetProperty
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
 - IAzApplicationGroup.SetProperty
 - AzApplicationGroup.SetProperty
---

# IAzApplicationGroup::SetProperty


## -description

The <b>SetProperty</b> method sets the specified value to the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property  to set. The following table shows the possible values.

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_TYPE"></a><a id="az_prop_group_type"></a><dl>
<dt><b>AZ_PROP_GROUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_LDAP_QUERY"></a><a id="az_prop_group_ldap_query"></a><dl>
<dt><b>AZ_PROP_GROUP_LDAP_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_ldapquery">LdapQuery</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property

</td>
</tr>
</table>

### -param varProp [in]

Value to set to the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object property  specified by the <i>lPropId</i> parameter. The following table shows the type of data that must be used depending on the value of the <i>lPropId</i> parameter.

<table>
<tr>
<th><i>lPropId</i> value</th>
<th>Data type (C++/Visual Basic)</th>
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
<td width="40%"><a id="AZ_PROP_GROUP_LDAP_QUERY"></a><a id="az_prop_group_ldap_query"></a><dl>
<dt><b>AZ_PROP_GROUP_LDAP_QUERY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GROUP_TYPE"></a><a id="az_prop_group_type"></a><dl>
<dt><b>AZ_PROP_GROUP_TYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>LONG</b>/<b>Long</b>

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

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.