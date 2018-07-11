---
UID: NF:wmsdkidl.IWMHeaderInfo.SetAttribute
title: IWMHeaderInfo::SetAttribute
author: windows-sdk-content
description: The SetAttribute method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::AddAttribute, and should not be used.
old-location: wmformat\iwmheaderinfo_setattribute.htm
old-project: wmformat
ms.assetid: 174969a2-4fe2-477b-9990-051d23bf8a29
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMHeaderInfo interface [windows Media Format],SetAttribute method, IWMHeaderInfo.SetAttribute, IWMHeaderInfo2 interface [windows Media Format],SetAttribute method, IWMHeaderInfo2::SetAttribute, IWMHeaderInfo3 interface [windows Media Format],SetAttribute method, IWMHeaderInfo3::SetAttribute, IWMHeaderInfo::SetAttribute, IWMHeaderInfoSetAttribute, SetAttribute, SetAttribute method [windows Media Format], SetAttribute method [windows Media Format],IWMHeaderInfo interface, SetAttribute method [windows Media Format],IWMHeaderInfo2 interface, SetAttribute method [windows Media Format],IWMHeaderInfo3 interface, wmformat.iwmheaderinfo_setattribute, wmsdkidl/IWMHeaderInfo2::SetAttribute, wmsdkidl/IWMHeaderInfo3::SetAttribute, wmsdkidl/IWMHeaderInfo::SetAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
 - qasf.dll
api_name:
 - IWMHeaderInfo.SetAttribute
 - IWMHeaderInfo2.SetAttribute
 - IWMHeaderInfo3.SetAttribute
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::SetAttribute


## -description



The <b>SetAttribute</b> method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by <a href="https://msdn.microsoft.com/15ecb34d-f70d-43a3-b369-2d9c2532945e">IWMHeaderInfo3::AddAttribute</a>, and should not be used.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. To set a file-level attribute, pass zero.


### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.


### -param Type [in]

A value from the <b>WMT_ATTR_DATATYPE</b> enumeration type.


### -param pValue [in]

Pointer to a byte array containing the value of the attribute.


### -param cbLength [in]

The size of <i>pValue</i>, in bytes.


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
A parameter does not contain a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state, or no profile has been set.

</td>
</tr>
</table>
 




## -remarks



Refer to the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section for a list of predefined attributes. For predefined attributes, the <i>Type</i> parameter must match the data type defined for that attribute. For custom attributes, you can specify any type except WMT_TYPE_GUID, but the buffer size (given by <i>cbLength</i>) must match the type. See <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> for more information.

The <b>IWMHeaderInfo</b> interface does not support the WMT_TYPE_GUID data type. To use this data type, you must use the methods of the <b>IWMHeaderInfo3</b> interface.

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero. When setting attributes for MP3 files, the metadata editor will automatically insert a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

This method does not support attributes with values larger than 64 kilobytes. To include large attributes in your file, use the methods of the <b>IWMHeaderInfo3</b> interface.

The writer object supports this method only before the <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a> method has been called. The reader and synchronous reader objects do not support this method.

Before you can use this method through the <b>IWMHeaderInfo</b> interface of a writer object to set <a href="wmformat_glossary.htm">DRM</a> attributes, you must set a profile for the writer to use.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.




## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>



<a href="https://msdn.microsoft.com/905fdf2c-a398-457e-80e9-aac124301f99">IWMHeaderInfo::GetAttributeByIndex</a>



<a href="https://msdn.microsoft.com/8941b989-f052-4e61-a64a-06748947fcf4">IWMHeaderInfo::GetAttributeByName</a>



<a href="https://msdn.microsoft.com/d5f0be62-4f15-45ca-8593-f5703a1f932a">IWMHeaderInfo::GetAttributeCount</a>



<a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a>
 

 

