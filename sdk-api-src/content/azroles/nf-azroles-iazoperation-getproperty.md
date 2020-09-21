---
UID: NF:azroles.IAzOperation.GetProperty
title: IAzOperation::GetProperty (azroles.h)
description: Returns the IAzOperation object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_NAME","AZ_PROP_OPERATION_ID","AZ_PROP_WRITABLE","AzOperation object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzOperation object","GetProperty method [Security]","IAzOperation interface","IAzOperation interface [Security]","GetProperty method","IAzOperation.GetProperty","IAzOperation::GetProperty","azroles/IAzOperation::GetProperty","security.iazoperation_getproperty"]
old-location: security\iazoperation_getproperty.htm
tech.root: security
ms.assetid: 211def10-d696-4b23-b54c-21f1f9b8f7ff
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_OPERATION_ID, AZ_PROP_WRITABLE, AzOperation object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzOperation object, GetProperty method [Security],IAzOperation interface, IAzOperation interface [Security],GetProperty method, IAzOperation.GetProperty, IAzOperation::GetProperty, azroles/IAzOperation::GetProperty, security.iazoperation_getproperty
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
 - IAzOperation::GetProperty
 - azroles/IAzOperation::GetProperty
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
 - IAzOperation.GetProperty
 - AzOperation.GetProperty
---

# IAzOperation::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_applicationdata">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value will always be <b>FALSE</b> because this object cannot have child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_description">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the   <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_name">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_OPERATION_ID"></a><a id="az_prop_operation_id"></a><dl>
<dt><b>AZ_PROP_OPERATION_ID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the  <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_operationid">OperationID</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the  <a href="/windows/desktop/api/azroles/nf-azroles-iazoperation-get_writable">Writable</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object property.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.