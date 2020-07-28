---
UID: NF:wmsdkidl.IWMStreamList.GetStreams
title: IWMStreamList::GetStreams (wmsdkidl.h)
description: The GetStreams method retrieves an array of stream numbers that make up the list.
helpviewer_keywords: ["GetStreams","GetStreams method [windows Media Format]","GetStreams method [windows Media Format]","IWMStreamList interface","IWMStreamList interface [windows Media Format]","GetStreams method","IWMStreamList.GetStreams","IWMStreamList::GetStreams","IWMStreamListGetStreams","wmformat.iwmstreamlist_getstreams","wmsdkidl/IWMStreamList::GetStreams"]
old-location: wmformat\iwmstreamlist_getstreams.htm
tech.root: wmformat
ms.assetid: ef7e1141-284f-4570-8891-9f53b2da7229
ms.date: 12/05/2018
ms.keywords: GetStreams, GetStreams method [windows Media Format], GetStreams method [windows Media Format],IWMStreamList interface, IWMStreamList interface [windows Media Format],GetStreams method, IWMStreamList.GetStreams, IWMStreamList::GetStreams, IWMStreamListGetStreams, wmformat.iwmstreamlist_getstreams, wmsdkidl/IWMStreamList::GetStreams
f1_keywords:
- wmsdkidl/IWMStreamList.GetStreams
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
- IWMStreamList.GetStreams
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamList::GetStreams


## -description



The <b>GetStreams</b> method retrieves an array of stream numbers that make up the list.




## -parameters




### -param pwStreamNumArray [out]

Pointer to a <b>WORD</b> array containing the stream numbers. Pass <b>NULL</b> to retrieve the required size of the array.


### -param pcStreams [in, out]

On input, a pointer to a variable containing the size of the <i>pwStreamNumArray</i> array. On output, if the method succeeds, this variable contains the number of stream numbers entered into <i>pwStreamNumArray</i> by the method.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcStreams</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The input value of <i>pcStreams</i> is not large enough.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetStreams</b>. On the first call, pass <b>NULL</b> as <i>pwStreamNumArray</i>. On return, the value pointed to by <i>pcStreams</i> is set to the number of stream numbers in the stream number array. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pwStreamNumArray</i> on the second call.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList Interface</a>
 

 

