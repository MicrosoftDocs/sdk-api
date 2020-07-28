---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetProtocolName
title: IWMReaderAdvanced2::GetProtocolName (wmsdkidl.h)
description: The GetProtocolName method retrieves the name of the protocol that is being used.
helpviewer_keywords: ["GetProtocolName","GetProtocolName method [windows Media Format]","GetProtocolName method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetProtocolName method","IWMReaderAdvanced2.GetProtocolName","IWMReaderAdvanced2::GetProtocolName","IWMReaderAdvanced2GetProtocolName","wmformat.iwmreaderadvanced2_getprotocolname","wmsdkidl/IWMReaderAdvanced2::GetProtocolName"]
old-location: wmformat\iwmreaderadvanced2_getprotocolname.htm
tech.root: wmformat
ms.assetid: 056d5f3f-79bf-4e21-9f2c-cda05eaca13d
ms.date: 12/05/2018
ms.keywords: GetProtocolName, GetProtocolName method [windows Media Format], GetProtocolName method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetProtocolName method, IWMReaderAdvanced2.GetProtocolName, IWMReaderAdvanced2::GetProtocolName, IWMReaderAdvanced2GetProtocolName, wmformat.iwmreaderadvanced2_getprotocolname, wmsdkidl/IWMReaderAdvanced2::GetProtocolName
f1_keywords:
- wmsdkidl/IWMReaderAdvanced2.GetProtocolName
dev_langs:
- c++
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
- IWMReaderAdvanced2.GetProtocolName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced2::GetProtocolName


## -description



The <b>GetProtocolName</b> method retrieves the name of the protocol that is being used.




## -parameters




### -param pwszProtocol [out]

Pointer to a buffer that receives a string containing the protocol name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchProtocol [in, out]

On input, pointer to a variable containing the length of <i>pwszProtocol</i>, in characters. On output, the variable contains the length of the name, including the terminating <b>null</b> character.


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
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The protocol has not been determined, or no file is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcchProtocol</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetProtocolName</b>. On the first call, pass <b>NULL</b> for <i>pwszProtocol</i>. On return, the value pointed to by <i>pcchProtocol</i> is set to the number of wide characters, including the terminating <b>null</b>, required to hold the protocol name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszProtocol</i> on the second call.

The protocol name is a URL scheme, such as <i>mmsu</i>, <i>http</i>, or <i>file</i>. However, the protocol name can differ from the URL scheme specified in <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>, because the reader object might use protocol rollover to find the best protocol. Also, the returned string might be "File" for local file content, or "Cache" for content saved in the cache.

This method can return an empty string if the protocol name cannot be determined.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>
 

 

