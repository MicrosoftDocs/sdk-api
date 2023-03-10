---
UID: NF:wmsdkidl.IWMReaderAdvanced4.SendLogParams
title: IWMReaderAdvanced4::SendLogParams (wmsdkidl.h)
description: The SendLogParams method sends log entries to the originating server. Call this method after calling AddLogParam.
helpviewer_keywords: ["IWMReaderAdvanced4 interface [windows Media Format]","SendLogParams method","IWMReaderAdvanced4.SendLogParams","IWMReaderAdvanced4::SendLogParams","IWMReaderAdvanced4SendLogParams","SendLogParams","SendLogParams method [windows Media Format]","SendLogParams method [windows Media Format]","IWMReaderAdvanced4 interface","wmformat.iwmreaderadvanced4_sendlogparams","wmsdkidl/IWMReaderAdvanced4::SendLogParams"]
old-location: wmformat\iwmreaderadvanced4_sendlogparams.htm
tech.root: wmformat
ms.assetid: 3b345573-bdca-4a1f-b272-716e2ca4c88c
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced4 interface [windows Media Format],SendLogParams method, IWMReaderAdvanced4.SendLogParams, IWMReaderAdvanced4::SendLogParams, IWMReaderAdvanced4SendLogParams, SendLogParams, SendLogParams method [windows Media Format], SendLogParams method [windows Media Format],IWMReaderAdvanced4 interface, wmformat.iwmreaderadvanced4_sendlogparams, wmsdkidl/IWMReaderAdvanced4::SendLogParams
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderAdvanced4::SendLogParams
 - wmsdkidl/IWMReaderAdvanced4::SendLogParams
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
 - IWMReaderAdvanced4.SendLogParams
---

# IWMReaderAdvanced4::SendLogParams


## -description

The <b>SendLogParams</b> method sends log entries to the originating server. Call this method after calling <b>AddLogParam</b>.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The reader is not streaming content from a remote server.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-addlogparam">IWMReaderAdvanced4::AddLogParam</a>
