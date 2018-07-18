---
UID: NF:msctf.ITfReadOnlyProperty.GetType
title: ITfReadOnlyProperty::GetType
author: windows-sdk-content
description: ITfReadOnlyProperty::GetType method
old-location: tsf\itfreadonlyproperty_gettype.htm
old-project: TSF
ms.assetid: a0c47d13-c290-4efe-ad73-6dcb654dc18f
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GUID_TFCAT_PROPSTYLE_CUSTOM, GUID_TFCAT_PROPSTYLE_STATIC, GUID_TFCAT_PROPSTYLE_STATICCOMPACT, GetType, GetType method [Text Services Framework], GetType method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetType method, ITfReadOnlyProperty.GetType, ITfReadOnlyProperty::GetType, _tsf_itfreadonlyproperty_gettype_ref, msctf/ITfReadOnlyProperty::GetType, tsf.itfreadonlyproperty_gettype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReadOnlyProperty.GetType
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

