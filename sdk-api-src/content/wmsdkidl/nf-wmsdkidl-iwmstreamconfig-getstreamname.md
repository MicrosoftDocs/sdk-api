---
UID: NF:wmsdkidl.IWMStreamConfig.GetStreamName
title: IWMStreamConfig::GetStreamName
author: windows-sdk-content
description: The GetStreamName method retrieves the stream name.
old-location: wmformat\iwmstreamconfig_getstreamname.htm
old-project: wmformat
ms.assetid: 86c65cfe-d482-461b-a187-ce1ce9a30609
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetStreamName, GetStreamName method [windows Media Format], GetStreamName method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetStreamName method, IWMStreamConfig.GetStreamName, IWMStreamConfig::GetStreamName, IWMStreamConfigGetStreamName, wmformat.iwmstreamconfig_getstreamname, wmsdkidl/IWMStreamConfig::GetStreamName
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
api_name:
 - IWMStreamConfig.GetStreamName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig::GetStreamName


## -description



The <b>GetStreamName</b> method retrieves the stream name.




## -parameters




### -param pwszStreamName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the stream name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchStreamName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszStreamName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the name, including the terminating <b>null</b> character.


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
The <i>pcchStreamName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The name value contained in the <i>pcchStreamName</i> parameter is too large for the <i>pwszStreamName</i> array.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetStreamName</b>. On the first call, pass <b>NULL</b> as <i>pwszStreamName</i>. On return, the value pointed to by <i>pcchStreamName</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the stream name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszStreamName</i> on the second call.

The stream name is not written to the header section of an ASF file. If you obtain the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface from the reader object or synchronous reader object, you cannot retrieve the original stream name.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/a8dc8c37-da52-4d0f-b143-aaa45e6f77b8">IWMStreamConfig::GetStreamType</a>



<a href="https://msdn.microsoft.com/90ab1591-eee7-4504-8d7f-475d90fa3b40">IWMStreamConfig::SetStreamName</a>
 

 

