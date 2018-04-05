---
UID: NF:azroles.IAzTask.SetProperty
title: IAzTask::SetProperty method
author: windows-driver-content
description: Sets the specified value to the IAzTask object property with the specified property ID.
old-location: security\iaztask_setproperty.htm
old-project: SecAuthZ
ms.assetid: 515d23f6-fcd9-4838-8910-2675211dfc48
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_DESCRIPTION, AZ_PROP_IS_ROLE_DEFINITION, AZ_PROP_NAME, AZ_PROP_TASK_BIZRULE, AZ_PROP_TASK_BIZRULE_LANGUAGE, AZ_PROP_TASK_IS_ROLE_DEFINITION, AzTask object [Security], SetProperty method, IAzTask, IAzTask interface [Security], SetProperty method, IAzTask::SetProperty, SetProperty method [Security], SetProperty method [Security], AzTask object, SetProperty method [Security], IAzTask interface, SetProperty,IAzTask.SetProperty, azroles/IAzTask::SetProperty, security.iaztask_setproperty
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzTask.SetProperty
-	AzTask.SetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::SetProperty method


## -description


The <b>SetProperty</b> method sets the specified value to the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property  to set. The following table shows the possible values.

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
Also  accessed through the <a href="https://msdn.microsoft.com/0a3939ee-6449-4eef-bb23-11e6d7018f04">ApplicationData</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE"></a><a id="az_prop_task_bizrule"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/cf3d87af-5320-4fe0-b513-e242f8a1dd1b">BizRule</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE_LANGUAGE"></a><a id="az_prop_task_bizrule_language"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_IS_ROLE_DEFINITION"></a><a id="az_prop_task_is_role_definition"></a><dl>
<dt><b>AZ_PROP_TASK_IS_ROLE_DEFINITION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/fef32545-de7e-4516-a289-b9ddf45b7c81">IsRoleDefinition</a>  property

</td>
</tr>
</table>
 


### -param varProp [in]

Value to set to the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property  specified by the <i>lPropId</i> parameter. The following table shows the type of data that must be used depending on the value of the <i>lPropId</i> parameter.

<table>
<tr>
<th><i>lPropId</i> value</th>
<th>Data type</th>
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
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE"></a><a id="az_prop_task_bizrule"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE_LANGUAGE"></a><a id="az_prop_task_bizrule_language"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE_LANGUAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_IS_ROLE_DEFINITION"></a><a id="az_prop_is_role_definition"></a><dl>
<dt><b>AZ_PROP_IS_ROLE_DEFINITION</b></dt>
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



The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a> method to persist any changes made by this method.



