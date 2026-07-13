---
UID: NF:wmsdkidl.IWMStreamList.RemoveStream
title: IWMStreamList::RemoveStream (wmsdkidl.h)
description: The RemoveStream method removes a stream from the list.
helpviewer_keywords: ["IWMStreamList interface [windows Media Format]","RemoveStream method","IWMStreamList.RemoveStream","IWMStreamList::RemoveStream","IWMStreamListRemoveStream","RemoveStream","RemoveStream method [windows Media Format]","RemoveStream method [windows Media Format]","IWMStreamList interface","wmformat.iwmstreamlist_removestream","wmsdkidl/IWMStreamList::RemoveStream"]
old-location: wmformat\iwmstreamlist_removestream.htm
tech.root: wmformat
ms.assetid: 3b69f516-a321-49f1-a299-666143eaf8a5
ms.date: 4/26/2023
ms.keywords: IWMStreamList interface [windows Media Format],RemoveStream method, IWMStreamList.RemoveStream, IWMStreamList::RemoveStream, IWMStreamListRemoveStream, RemoveStream, RemoveStream method [windows Media Format], RemoveStream method [windows Media Format],IWMStreamList interface, wmformat.iwmstreamlist_removestream, wmsdkidl/IWMStreamList::RemoveStream
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
 - IWMStreamList::RemoveStream
 - wmsdkidl/IWMStreamList::RemoveStream
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
 - IWMStreamList.RemoveStream
---

# IWMStreamList::RemoveStream


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveStream</b> method removes a stream from the list.

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
<dt><b>NS_E_NOMATCHING_ELEMENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>wStreamNum</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

The <b>RemoveStream</b> method also removes the stream from any mutual exclusion objects that the stream belongs to.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream">IWMStreamList::AddStream</a>