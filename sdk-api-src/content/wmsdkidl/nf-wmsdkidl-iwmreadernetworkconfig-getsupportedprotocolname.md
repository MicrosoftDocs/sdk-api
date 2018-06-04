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

# IWMReaderNetworkConfig::GetSupportedProtocolName


## -description



The <b>GetSupportedProtocolName</b> method retrieves a protocol name by index.




## -parameters




### -param dwProtocolNum [in]

Specifies protocol name to retrieve, indexed from zero. To get the number of supported protocols, call the <a href="https://msdn.microsoft.com/6e249d8f-0351-452f-9b53-86f77df2fd70">IWMReaderNetworkConfig::GetNumProtocolsSupported</a> method.


### -param pwszProtocolName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the protocol name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchProtocolName [in, out]

On input, pointer to a <b>DWORD</b> containing the length of the <i>pwszProtocolName</i>, in characters. On output, pointer to the length of the protocol name, including the terminating <b>null</b> character.


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
<b>NULL</b> or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetSupportedProtocolName</b>. On the first call, pass <b>NULL</b> for <i>pwszProtocoName</i>. On return, the value pointed to by <i>pcchProtocolName</i> is set to the number of wide characters, including the terminating <b>null</b>, required to hold the protocol name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszProtocolName</i> on the second call.

Use this method along with <b>GetNumProtocolsSupported</b> to iterate through the network protocols supported by the reader object.

This method only returns a list of protocols that are used to receive content from Windows Media servers. Protocols that are only used for retrieving content from local sources, or non-Windows Media servers (such as Web servers) are not included in this list.

<div class="alert"><b>Note</b>  The HTTPS support works only when downloading content from a Web server (because the player is using WININET). Streaming protocols supported are HTTP, RTSP, MMS, and, for multicasting, ASFM (by opening an ASF file with an .nsc extension). Download support includes HTTP, HTTPS, and FTP.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>
 

 

