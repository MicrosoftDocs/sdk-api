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

# IWMCodecInfo3::GetCodecProp


## -description



The <b>GetCodecProp</b> method retrieves a codec property.




## -parameters




### -param guidType [in]

GUID identifying the major type of digital media. This must be one of the following constants.

<table>
<tr>
<th>
                  Constant
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMMEDIATYPE_Video</td>
<td>Specifies a video codec.</td>
</tr>
<tr>
<td>WMMEDIATYPE_Audio</td>
<td>Specifies an audio codec.</td>
</tr>
</table>
 


### -param dwCodecIndex [in]

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major type, use the <a href="https://msdn.microsoft.com/873f8d03-5d7b-424c-91f3-e7c8156565be">IWMCodecInfo::GetCodecInfoCount</a> method.


### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to retrieve.

The following table lists the codec properties you can retrieve. The property dictates the data type and value; this information is also included in the table.

<table>
<tr>
<th>
                  Global constant
                </th>
<th>
                  Data type
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>g_wszComplexityMax</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the maximum complexity value for the codec. Codec complexity applies only to video codecs. The range of complexity values is from 0 to this value.</td>
</tr>
<tr>
<td>g_wszComplexityOffline</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the suggested complexity value for the codec when encoding files for local playback. Codec complexity applies only to video codecs. The range of complexity values is from 0 to the value retrieved with g_wszComplexityMax.</td>
</tr>
<tr>
<td>g_wszComplexityLive</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the suggested complexity value for the codec when encoding files for streaming playback. Codec complexity applies only to video codecs. The range of complexity values is from 0 to the value retrieved with g_wszComplexityMax.</td>
</tr>
<tr>
<td>g_wszIsVBRSupported</td>
<td><b>WMT_TYPE_BOOL</b></td>
<td>The value indicates whether the codec supports VBR.</td>
</tr>
</table>
 




### -param pType [out]

Pointer to a variable that will receive a member of the <b>WMT_ATTR_DATATYPE</b> enumeration type. This value specifies the type of information returned to the buffer at <i>pValue</i>.


### -param pValue [out]

Pointer to a buffer that will receive the value of the property. The data returned is of a type specified by <i>pType</i>.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> value specifying the length of the buffer at <i>pValue</i>.


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
<i>pszName</i> or <i>pType</i> or <i>pdwSize</i> is <b>NULL</b>.

OR

<i>guidType</i> specifies an invalid input type.

OR

<i>pszName</i> specifies an invalid property name.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetCodecProp</b> for each property you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value of <i>pdwSize</i> will be set to the buffer size required to hold the value of the specified property. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/fd882612-1f60-4b51-a180-0d34d78c99dd">IWMCodecInfo3 Interface</a>
 

 

