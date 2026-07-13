---
UID: NF:azroles.IAzScope.AddPropertyItem
title: IAzScope::AddPropertyItem (azroles.h)
description: Adds the specified principal to the specified list of principals. (IAzScope.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_POLICY_ADMINS","AZ_PROP_POLICY_ADMINS_NAME","AZ_PROP_POLICY_READERS","AZ_PROP_POLICY_READERS_NAME","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzScope object","AddPropertyItem method [Security]","IAzScope interface","AzScope object [Security]","AddPropertyItem method","IAzScope interface [Security]","AddPropertyItem method","IAzScope.AddPropertyItem","IAzScope::AddPropertyItem","azroles/IAzScope::AddPropertyItem","security.iazscope_addpropertyitem"]
old-location: security\iazscope_addpropertyitem.htm
tech.root: security
ms.assetid: 5170079b-9ea6-417c-87f2-bb8835225911
ms.date: 12/05/2018
ms.keywords: AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzScope object, AddPropertyItem method [Security],IAzScope interface, AzScope object [Security],AddPropertyItem method, IAzScope interface [Security],AddPropertyItem method, IAzScope.AddPropertyItem, IAzScope::AddPropertyItem, azroles/IAzScope::AddPropertyItem, security.iazscope_addpropertyitem
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
 - IAzScope::AddPropertyItem
 - azroles/IAzScope::AddPropertyItem
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
 - IAzScope.AddPropertyItem
 - AzScope.AddPropertyItem
---

# IAzScope::AddPropertyItem


## -description

The <b>AddPropertyItem</b> method adds the specified principal to the specified list of principals.

## -parameters

### -param lPropId [in]

Property ID of the  list of principals to which to add the principal specified by the <i>varProp</i> parameter. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS"></a><a id="az_prop_policy_admins"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyadministrator">AddPolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyadministratorname">AddPolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyreader">AddPolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-addpolicyreadername">AddPolicyReaderName</a> method

</td>
</tr>
</table>

### -param varProp [in]

Principal to add to the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS or AZ_PROP_POLICY_READERS is specified for the <i>lPropId</i> parameter, the string is the text form of the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the Windows account to add to the list. If AZ_PROP_POLICY_ADMINS_NAME or AZ_PROP_POLICY_READERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-submit">Submit</a> method to persist any changes made by this method.
