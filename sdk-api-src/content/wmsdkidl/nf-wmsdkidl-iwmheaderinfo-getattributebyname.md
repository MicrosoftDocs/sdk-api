---
UID: NF:wmsdkidl.IWMHeaderInfo.GetAttributeByName
title: IWMHeaderInfo::GetAttributeByName
author: windows-sdk-content
description: The GetAttributeByName method returns a descriptive attribute that is stored in the header section of the ASF file.
old-location: wmformat\iwmheaderinfo_getattributebyname.htm
old-project: wmformat
ms.assetid: 8941b989-f052-4e61-a64a-06748947fcf4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetAttributeByName, GetAttributeByName method [windows Media Format], GetAttributeByName method [windows Media Format],IWMHeaderInfo interface, GetAttributeByName method [windows Media Format],IWMHeaderInfo2 interface, GetAttributeByName method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo.GetAttributeByName, IWMHeaderInfo2 interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo2::GetAttributeByName, IWMHeaderInfo3 interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo3::GetAttributeByName, IWMHeaderInfo::GetAttributeByName, IWMHeaderInfoGetAttributeByName, wmformat.iwmheaderinfo_getattributebyname, wmsdkidl/IWMHeaderInfo2::GetAttributeByName, wmsdkidl/IWMHeaderInfo3::GetAttributeByName, wmsdkidl/IWMHeaderInfo::GetAttributeByName
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
 - IWMHeaderInfo.GetAttributeByName
 - IWMHeaderInfo2.GetAttributeByName
 - IWMHeaderInfo3.GetAttributeByName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::GetAttributeByName


## -description



The <b>GetAttributeByName</b> method returns a descriptive attribute that is stored in the header section of the ASF file. Now that attribute names can be duplicated in a file, this method is obsolete. To find attributes of a particular name, use <a href="https://msdn.microsoft.com/15c8f0c2-f2d4-441a-b6a9-774da820d03c">IWMHeaderInfo3::GetAttributeIndices</a>.




## -parameters




### -param pwStreamNum [in, out]

Pointer to a <b>WORD</b> containing the stream number, or zero to indicate any stream. Although this parameter is a pointer, the method does not change the value.


### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.


### -param pType [out]

Pointer to a variable that receives a value from the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type. The returned value specifies the data type of the attribute.


### -param pValue [out]

Pointer to a byte array that receives the value of the attribute. The caller must allocate the array. To determine the required array size, set this parameter to <b>NULL</b> and check the value returned in the <i>pcbLength</i> parameter.


### -param pcbLength [in, out]

On input, the length of the <i>pValue</i> array, in bytes. On output, if the method succeeds, the actual number of bytes that were written to <i>pValue</i>.


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
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified attribute is not defined in this file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwStreamNum</i> is not a valid stream number, <i>pszName</i> does not point to a wide-character string, or another parameter does not contain a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not a valid pointer.

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



Typically, an application should call this method twice for each attribute that it retrieves. On the first call, set the <i>pValue</i> parameter to <b>NULL</b>. The <i>pcbLength</i> parameter receives the buffer size needed to hold the attribute value. Then, allocate a sufficient byte array and call the method again, passing the address of the array in the <i>pType</i> parameter. The method fills the buffer with the value of the attribute. Coerce the buffer to the data type indicated by the value returned in <i>pType</i>.

If the file does not contain the specified attribute, the method might return ASF_E_NOTFOUND. The method can also succeed but return the value zero for <i>pcbLength</i>.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero.

For a list of all the predefined attributes, see <a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>.


#### Examples

The following example code shows how to retrieve the "Title" attribute.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
IWMHeaderInfo *pInfo;
WORD wStreamNum = 0;
WMT_ATTR_DATATYPE Type;
WORD cbLength;
//
// First, retrieve the length of the string, and allocate memory.
//
hr = pInfo-&gt;GetAttributeByName( &amp;wStreamNum, L"Title", 
                                &amp;Type, NULL, &amp;cbLength );
if( FAILED( hr ) )
{
    return( hr );
}
WCHAR *pwszTitle = (WCHAR *) new BYTE[ cbLength ];
if( !pwszTitle )
{
    return( E_OUTOFMEMORY );
}
//
// Now, retrieve the string itself.
//
hr = pInfo-&gt;GetAttributeByName( &amp;wStreamNum, L"Title", &amp;Type, 
                                (BYTE *) pwszTitle, &amp;cbLength );
if( FAILED( hr ) )
{
    return( hr );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/174969a2-4fe2-477b-9990-051d23bf8a29">IWMHeaderInfo::SetAttribute</a>



<a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a>
 

 

