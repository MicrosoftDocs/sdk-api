---
UID: NF:wmsdkidl.IWMStreamList.AddStream
title: IWMStreamList::AddStream (wmsdkidl.h)
description: The AddStream method adds a stream to the list.
helpviewer_keywords: ["AddStream","AddStream method [windows Media Format]","AddStream method [windows Media Format]","IWMStreamList interface","IWMStreamList interface [windows Media Format]","AddStream method","IWMStreamList.AddStream","IWMStreamList::AddStream","IWMStreamListAddStream","wmformat.iwmstreamlist_addstream","wmsdkidl/IWMStreamList::AddStream"]
old-location: wmformat\iwmstreamlist_addstream.htm
tech.root: wmformat
ms.assetid: 20aeed9d-029b-4b60-9ff3-14555bd53eb9
ms.date: 12/05/2018
ms.keywords: AddStream, AddStream method [windows Media Format], AddStream method [windows Media Format],IWMStreamList interface, IWMStreamList interface [windows Media Format],AddStream method, IWMStreamList.AddStream, IWMStreamList::AddStream, IWMStreamListAddStream, wmformat.iwmstreamlist_addstream, wmsdkidl/IWMStreamList::AddStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMStreamList::AddStream
 - wmsdkidl/IWMStreamList::AddStream
dev_langs:
 - c++
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
 - IWMStreamList.AddStream
---

# IWMStreamList::AddStream


## -description

The <b>AddStream</b> method adds a stream to the list.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamlist-removestream">IWMStreamList::RemoveStream</a>