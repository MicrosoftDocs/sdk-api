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

# IWMCodecInfo3::GetCodecEnumerationSetting


## -description



The <b>GetCodecEnumerationSetting</b> method retrieves the current value for one codec enumeration setting. Codec enumeration settings dictate the codec formats that can be enumerated by the methods of <a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo</a>. You can change codec enumeration settings in order to retrieve codec formats supporting specific features by calling <a href="https://msdn.microsoft.com/5b4883b8-63c0-40ff-b13f-303d30ebfe15">IWMCodecInfo3::SetCodecEnumerationSetting</a>.




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

Pointer to a wide-character <b>null</b>-terminated string containing the name of the enumeration setting. Use one of the following constants.

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
<td>Use to enumerate the supported codec formats that use variable bit rate (VBR) encoding.The value returned in <i>pValue</i> is a <b></b>BOOL.

</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>Use to enumerate the supported codec formats that use a number of passes equal to the value in <i>pValue</i>.The value returned in <i>pValue</i> is a <b>DWORD</b> specifying the number of passes.

</td>
</tr>
</table>
 


### -param pType [out]

Pointer to a <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration value specifying the data type of the value returned in <i>pValue</i>.


### -param pValue [out]

Pointer to a <b>BYTE</b> array containing the codec enumeration data. The data type and meaning of the data returned in this array depends on the setting specified by <i>pszName</i>. You can set this value to <b>NULL</b> to retrieve the required size of the array in <i>pdwSize</i>.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size of the setting value in bytes. If you set <i>pValue</i> to <b>NULL</b>, this value will be set to the size required to hold the setting value.


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
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The enumeration setting specified is not valid for the codec.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fd882612-1f60-4b51-a180-0d34d78c99dd">IWMCodecInfo3 Interface</a>



<a href="https://msdn.microsoft.com/5b4883b8-63c0-40ff-b13f-303d30ebfe15">SetCodecEnumerationSetting</a>
 

 

