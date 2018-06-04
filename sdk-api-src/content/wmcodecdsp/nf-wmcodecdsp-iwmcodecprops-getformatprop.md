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

# IWMCodecProps::GetFormatProp


## -description



Retrieves a format property for an output media type. Use this method to get information about enumerated audio formats.



## -parameters




### -param pmt [in]

Pointer to the output media type.


### -param pszName [in]

Wide-character, null-terminated string containing the property name. The properties listed in the following table are supported only through the IWMCodecProps interface.

<table>
<tr>
<th>Property name constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="g_wszSpeechFormatCaps"></a><a id="g_wszspeechformatcaps"></a><a id="G_WSZSPEECHFORMATCAPS"></a><dl>
<dt><b>g_wszSpeechFormatCaps</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the speech modes available for the format (used only by the Windows Media Audio 9 Voice codec). Value contains flags identical to the values used to specify the mode for <a href="https://msdn.microsoft.com/8425cdab-e43c-41ca-9c20-09ab6a5f06f4">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a>.

</td>
</tr>
</table>
 

The properties in the following list are also supported. They are used with <b>IPropertyBag</b> for video. 

<ul>
<li>
<a href="https://msdn.microsoft.com/e6826802-99b7-4a38-9b58-8a9cb8b753fb">MFPKEY_VBRENABLED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e45d583a-323b-4394-9df3-949a3f713708">MFPKEY_VBRQUALITY</a>
</li>
</ul>

### -param pType [out]

Address of a variable that receives the data type of the property value.


### -param pValue [out]

Address of the byte buffer that receives the property value.


### -param pdwSize [in, out]

Pointer to the size of the value buffer, in bytes. If pValue is <b>NULL</b>, the method will set this value to the size required.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b49e506b-8c87-44b9-be6c-b9a33f6c9ecb">IWMCodecProps Interface</a>



<a href="https://msdn.microsoft.com/e6826802-99b7-4a38-9b58-8a9cb8b753fb">MFPKEY_VBRENABLED</a>



<a href="https://msdn.microsoft.com/e45d583a-323b-4394-9df3-949a3f713708">MFPKEY_VBRQUALITY</a>
 

 

