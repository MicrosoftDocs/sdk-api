---
UID: NF:azroles.IAzOperation.GetProperty
title: IAzOperation::GetProperty
author: windows-sdk-content
description: Returns the IAzOperation object property with the specified property ID.
old-location: security\iazoperation_getproperty.htm
tech.root: SecAuthZ
ms.assetid: 211def10-d696-4b23-b54c-21f1f9b8f7ff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_OPERATION_ID, AZ_PROP_WRITABLE, AzOperation object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzOperation object, GetProperty method [Security],IAzOperation interface, IAzOperation interface [Security],GetProperty method, IAzOperation.GetProperty, IAzOperation::GetProperty, azroles/IAzOperation::GetProperty, security.iazoperation_getproperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzOperation.GetProperty
 - AzOperation.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzOperation.GetProperty
: 
---

# IAzOperation::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object property  to return. The following table shows the possible values.

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
Also accessed through the <a href="https://msdn.microsoft.com/d4d22aae-6ca3-4a97-aa44-fa07674dc556">ApplicationData</a> property

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
Also accessed through the <a href="https://msdn.microsoft.com/9f39032d-7624-43f8-91a4-6e616e691156">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the   <a href="https://msdn.microsoft.com/e1ebacda-513c-49f7-bb36-15229fdb0b3b">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_OPERATION_ID"></a><a id="az_prop_operation_id"></a><dl>
<dt><b>AZ_PROP_OPERATION_ID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the  <a href="https://msdn.microsoft.com/3466dea1-b005-40fc-87d1-29b5e033f6a0">OperationID</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the  <a href="https://msdn.microsoft.com/16745237-23d9-4818-b8f8-de93405ae9ac">Writable</a> property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/en-us/library/Aa377899(v=VS.85).aspx">IAzOperation</a> object property.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



