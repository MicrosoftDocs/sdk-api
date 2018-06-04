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

# IWMHeaderInfo3::AddAttribute


## -description



The <b>AddAttribute</b> method adds a metadata attribute. To change the value of an existing attribute, use the <a href="https://msdn.microsoft.com/503099e9-a1a9-406f-abc9-7c632d757cca">IWMHeaderInfo3::ModifyAttribute</a> method.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number of the stream to which the attribute applies. Setting this value to zero indicates an attribute that applies to the entire file.


### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.


### -param pwIndex [out]

Pointer to a <b>WORD</b>. On successful completion of the method, this value is set to the index assigned to the new attribute.


### -param Type [in]

Type of data used for the new attribute. For more information about the types of data supported, see <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a>.


### -param wLangIndex [in]

<b>WORD</b> containing the language index of the language to be associated with the new attribute. This is the index of the language in the language list for the file. Setting this value to zero indicates that the default language will be used. A default language is created and set according to the regional settings on the computer running your application.


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
<dt><b>NS_E_SDK_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by <i>dwLength</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number.

</td>
</tr>
</table>
 




## -remarks



This method appends a null character to the end of the string passed in <i>pwszName</i> if one is not present. In this case, the buffer needed to retrieve the attribute name will be two bytes larger than the input buffer.

When setting attributes for MP3 files, the metadata editor automatically inserts a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

<div class="alert"><b>Note</b>  Be careful to use the correct type representations of values. For example, when setting WM/MediaClassPrimaryID or WM/MediaClassSecondaryID attributes the values need to be represented as GUIDs converted to a byte array instead of strings converted to a byte array.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

