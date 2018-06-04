---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _EAP_CONFIG_INPUT_FIELD_ARRAY structure


## -description


 The <b>EAP_CONFIG_INPUT_FIELD_ARRAY</b> structure contains a set of <a href="https://msdn.microsoft.com/2b321f26-fb40-44e5-b483-52d85cb54c8c">EAP_CONFIG_INPUT_FIELD_DATA</a>   structures that collectively contain the user input field data obtained from the user.


## -struct-fields




### -field dwVersion

The version of the <a href="https://msdn.microsoft.com/2b321f26-fb40-44e5-b483-52d85cb54c8c">EAP_CONFIG_INPUT_FIELD_DATA</a>   structures pointed to by  <b>pFields</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAP_CREDENTIAL_VERSION"></a><a id="eap_credential_version"></a><dl>
<dt><b>EAP_CREDENTIAL_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The version of the EAP credentials supplied by the user.

</td>
</tr>
</table>
 


### -field dwNumberOfFields

 The total number of elements in the array specified by  <b>pFields</b>.


### -field pFields.size_is

 


### -field pFields.size_is.dwNumberOfFields

 


### -field pFields

Pointer to an array of <a href="https://msdn.microsoft.com/2b321f26-fb40-44e5-b483-52d85cb54c8c">EAP_CONFIG_INPUT_FIELD_DATA</a> structures that contain specific user input data obtained from an EAP configuration dialog box.


#### - dwSize

The size, in bytes, of the array pointed to by <b>pFields</b>.


## -remarks



The <b>EAP_CONFIG_INPUT_FIELD_ARRAY</b> structure can be employed to support Single-Sign-On (SSO).




## -see-also




<a href="https://msdn.microsoft.com/2b321f26-fb40-44e5-b483-52d85cb54c8c">EAP_CONFIG_INPUT_FIELD_DATA</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

