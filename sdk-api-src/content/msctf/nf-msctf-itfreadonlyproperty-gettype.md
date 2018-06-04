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

# ITfReadOnlyProperty::GetType


## -description




## -parameters




### -param pguid [out]

Pointer to a <b>GUID</b> value that receives the property type identifier. This is the value that the property provider passed to <a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory</a> when the property was registered. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_STATIC"></a><a id="guid_tfcat_propstyle_static"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The property is a static property.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_STATICCOMPACT"></a><a id="guid_tfcat_propstyle_staticcompact"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_STATICCOMPACT</b></dt>
</dl>
</td>
<td width="60%">
The property is a static-compact property.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_CUSTOM"></a><a id="guid_tfcat_propstyle_custom"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_CUSTOM</b></dt>
</dl>
</td>
<td width="60%">
The property is a custom property.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory
      </a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>
 

 

