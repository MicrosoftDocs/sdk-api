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

# IWMHeaderInfo3::ModifyAttribute


## -description



The <b>ModifyAttribute</b> method modifies the settings of an existing attribute.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number to which the attribute applies. Pass zero for file-level attributes.


### -param wIndex [in]

<b>WORD</b> containing the index of the attribute to change.


### -param Type [in]

Type of data used for the new attribute value. For more information about the types of data supported, see <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a>.


### -param wLangIndex [in]

<b>WORD</b> containing the language index of the language to be associated with the new attribute. This is the index of the language in the language list for the file.


### -param pValue [in]

Pointer to an array of bytes containing the attribute value.


### -param dwLength [in]

<b>DWORD</b> containing the length of the attribute value, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An illegal parameter combination, data type, or attribute name was used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented on a reader object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_ATTRIBUTE_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The attribute cannot be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or there is no attribute at <i>wIndex</i>.

</td>
</tr>
</table>
 




## -remarks



You can use 0xFFFF for the stream number to specify an attribute using its global index. Global index values range from 0 to one less than the count of attributes received from a call to <a href="https://msdn.microsoft.com/8c56d7b6-4f59-450e-938c-b7d0bd37ea08">IWMHeaderInfo3::GetAttributeCountEx</a> where the stream number was set to 0xFFFF.

When setting attributes for MP3 files, the metadata editor will automatically insert a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.




## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

