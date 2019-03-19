---
UID: NF:wmsdkidl.IWMHeaderInfo.SetAttribute
title: IWMHeaderInfo::SetAttribute (wmsdkidl.h)
author: windows-sdk-content
description: The SetAttribute method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::AddAttribute, and should not be used.
old-location: wmformat\iwmheaderinfo_setattribute.htm
tech.root: wmformat
ms.assetid: 174969a2-4fe2-477b-9990-051d23bf8a29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMHeaderInfo interface [windows Media Format],SetAttribute method, IWMHeaderInfo.SetAttribute, IWMHeaderInfo2 interface [windows Media Format],SetAttribute method, IWMHeaderInfo2::SetAttribute, IWMHeaderInfo3 interface [windows Media Format],SetAttribute method, IWMHeaderInfo3::SetAttribute, IWMHeaderInfo::SetAttribute, IWMHeaderInfoSetAttribute, SetAttribute, SetAttribute method [windows Media Format], SetAttribute method [windows Media Format],IWMHeaderInfo interface, SetAttribute method [windows Media Format],IWMHeaderInfo2 interface, SetAttribute method [windows Media Format],IWMHeaderInfo3 interface, wmformat.iwmheaderinfo_setattribute, wmsdkidl/IWMHeaderInfo2::SetAttribute, wmsdkidl/IWMHeaderInfo3::SetAttribute, wmsdkidl/IWMHeaderInfo::SetAttribute
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IWMHeaderInfo::SetAttribute


## -description



The <b>SetAttribute</b> method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by <a href="https://msdn.microsoft.com/en-us/library/Dd798509(v=VS.85).aspx">IWMHeaderInfo3::AddAttribute</a>, and should not be used.




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



Refer to the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section for a list of predefined attributes. For predefined attributes, the <i>Type</i> parameter must match the data type defined for that attribute. For custom attributes, you can specify any type except WMT_TYPE_GUID, but the buffer size (given by <i>cbLength</i>) must match the type. See <a href="https://msdn.microsoft.com/en-us/library/Dd757834(v=VS.85).aspx">WMT_ATTR_DATATYPE</a> for more information.

The <b>IWMHeaderInfo</b> interface does not support the WMT_TYPE_GUID data type. To use this data type, you must use the methods of the <b>IWMHeaderInfo3</b> interface.

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero. When setting attributes for MP3 files, the metadata editor will automatically insert a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

This method does not support attributes with values larger than 64 kilobytes. To include large attributes in your file, use the methods of the <b>IWMHeaderInfo3</b> interface.

The writer object supports this method only before the <a href="https://msdn.microsoft.com/en-us/library/Dd757474(v=VS.85).aspx">IWMWriter::BeginWriting</a> method has been called. The reader and synchronous reader objects do not support this method.

Before you can use this method through the <b>IWMHeaderInfo</b> interface of a writer object to set <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">DRM</a> attributes, you must set a profile for the writer to use.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.




## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798504(v=VS.85).aspx">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798505(v=VS.85).aspx">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798508(v=VS.85).aspx">IWMHeaderInfo3 Interface</a>



<a href="https://msdn.microsoft.com/905fdf2c-a398-457e-80e9-aac124301f99">IWMHeaderInfo::GetAttributeByIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798519(v=VS.85).aspx">IWMHeaderInfo::GetAttributeByName</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798520(v=VS.85).aspx">IWMHeaderInfo::GetAttributeCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757834(v=VS.85).aspx">WMT_ATTR_DATATYPE</a>
 

 

