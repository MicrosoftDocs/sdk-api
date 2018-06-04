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

# IWMCodecInfo3::SetCodecEnumerationSetting


## -description



The <b>SetCodecEnumerationSetting</b> method sets the value of one codec enumeration setting. Codec enumeration settings dictate the codec formats that can be enumerated by the methods of <a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo</a>.




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

Pointer to a wide-character null-terminated string containing the name of the enumeration setting. Use one of the following constants.

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
<td>g_wszVBREnabled</td>
<td>Use to enumerate the supported codec formats that use variable bit rate (VBR) encoding.The value returned in <i>pValue</i> is a <b>BOOL</b>.

</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>Use to enumerate the supported codec formats that use a number of passes equal to the value in <i>pValue</i>.The value returned in <i>pValue</i> is a <b>DWORD</b> specifying the number of passes.

</td>
</tr>
</table>
 


### -param Type [in]

A <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> value specifying the data type of the value in <i>pValue</i>.


### -param pValue [in]

A pointer to a <b>BYTE</b> array containing the setting value.


### -param dwSize [in]


<b>DWORD</b> containing the size of the <i>pValue</i> <b>BYTE</b> array.


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
The method succeeded; the feature is supported by the codec.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The enumeration setting specified is not valid for the codec.

</td>
</tr>
</table>
 




## -remarks



The Windows Media Audio and Video 9 Series codecs can potentially enumerate four different sets of codec formats, as listed in the following table.

<table>
<tr>
<th></th>
<th>
              Constant bit rate (CBR) stream
            </th>
<th>
              Two-pass CBR stream
            </th>
<th>
              Quality-based variable bit rate (VBR) stream
            </th>
<th>
              Bit-rate-based VBR stream (constrained or unconstrained)
            </th>
</tr>
<tr>
<td>g_wszVBREnabled</td>
<td>FALSE</td>
<td>FALSE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>1</td>
<td>2</td>
<td>1</td>
<td>2</td>
</tr>
</table>
 

Not all codecs support all formats.

If you make a call to this method and get the NS_E_UNSUPPORTED_PROPERTY error code, then the codec does not support that feature. For example, if an attempt to set g_wszNumPasses returns NS_E_UNSUPPORTED_PROPERTY, the codec does not support multiple encoding passes.

The return value of a call made to this method does not guarantee support of a codec feature. For example, the Windows Media Audio 9 Lossless codec does not return NS_E_UNSUPPORTED_PROPERTY for calls that set the number of passes, even though the codec does not support two-pass encoding.




## -see-also




<a href="https://msdn.microsoft.com/9a8f34ef-4d52-47d4-b6d5-e6f07f27cc8d">GetCodecEnumerationSetting</a>



<a href="https://msdn.microsoft.com/fd882612-1f60-4b51-a180-0d34d78c99dd">IWMCodecInfo3 Interface</a>
 

 

