---
UID: NF:wmsdkidl.IWMWriterNetworkSink.GetHostURL
title: IWMWriterNetworkSink::GetHostURL
author: windows-sdk-content
description: The GetHostURL method retrieves the URL from which the stream is broadcast. Clients will access the stream from this URL.
old-location: wmformat\iwmwriternetworksink_gethosturl.htm
tech.root: wmformat
ms.assetid: 66d4747e-aec5-47bd-ac4a-dc052e964601
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetHostURL, GetHostURL method [windows Media Format], GetHostURL method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],GetHostURL method, IWMWriterNetworkSink.GetHostURL, IWMWriterNetworkSink::GetHostURL, IWMWriterNetworkSinkGetHostURL, wmformat.iwmwriternetworksink_gethosturl, wmsdkidl/IWMWriterNetworkSink::GetHostURL
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
api_name:
 - IWMWriterNetworkSink.GetHostURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterNetworkSink::GetHostURL


## -description



The <b>GetHostURL</b> method retrieves the URL from which the stream is broadcast. Clients will access the stream from this URL.




## -parameters




### -param pwszURL [out]

Pointer to buffer that receives a string containing the URL. To retrieve the length of the string, set this parameter to <b>NULL</b>.


### -param pcchURL [in, out]

On input, pointer to the size of <i>pwszURL</i>, in characters. On output, this parameter receives the length of the URL in characters, including the terminating <b>null</b> character.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, the values shown in the following table.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>pcchURL</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is not connected.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetHostURL</b>. On the first call, pass <b>NULL</b> as <i>pwszURL</i>. On return, the value pointed to by <i>pcchURL</i> is set to the number of characters, including the terminating <b>null</b> character, required to hold the URL. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszURL</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798761(v=VS.85).aspx">IWMWriterNetworkSink Interface</a>
 

 

