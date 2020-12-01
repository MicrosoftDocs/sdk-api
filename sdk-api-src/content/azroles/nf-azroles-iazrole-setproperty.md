---
UID: NF:azroles.IAzRole.SetProperty
title: IAzRole::SetProperty (azroles.h)
description: Sets the specified value to the IAzRole object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_DESCRIPTION","AZ_PROP_NAME","AzRole object [Security]","SetProperty method","IAzRole interface [Security]","SetProperty method","IAzRole.SetProperty","IAzRole::SetProperty","SetProperty","SetProperty method [Security]","SetProperty method [Security]","AzRole object","SetProperty method [Security]","IAzRole interface","azroles/IAzRole::SetProperty","security.iazrole_setproperty"]
old-location: security\iazrole_setproperty.htm
tech.root: security
ms.assetid: 0f1c4abe-69cc-4672-8a74-eaaf55fc6e88
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AzRole object [Security],SetProperty method, IAzRole interface [Security],SetProperty method, IAzRole.SetProperty, IAzRole::SetProperty, SetProperty, SetProperty method [Security], SetProperty method [Security],AzRole object, SetProperty method [Security],IAzRole interface, azroles/IAzRole::SetProperty, security.iazrole_setproperty
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
 - IAzRole::SetProperty
 - azroles/IAzRole::SetProperty
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
 - IAzRole.SetProperty
 - AzRole.SetProperty
---

# IAzRole::SetProperty


## -description

The <b>SetProperty</b> method sets the specified value to the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property  to set. The following table shows the possible values.

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
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_applicationdata">ApplicationData</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_description">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_name">Name</a>  property

</td>
</tr>
</table>

### -param varProp [in]

The value to set to the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object property  specified by the <i>lPropId</i> parameter. The following table shows the type of data that must be used depending on the value of the <i>lPropId</i> parameter.

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

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.