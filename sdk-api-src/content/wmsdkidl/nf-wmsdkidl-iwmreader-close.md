---
UID: NF:wmsdkidl.IWMReader.Close
title: IWMReader::Close (wmsdkidl.h)
author: windows-sdk-content
description: The Close method deletes all outputs on the reader and releases the file resources.
old-location: wmformat\iwmreader_close.htm
tech.root: wmformat
ms.assetid: 3f320a0c-8586-4fc2-bd70-06ddda435cb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],Close method, IWMReader.Close, IWMReader::Close, IWMReaderClose, wmformat.iwmreader_close, wmsdkidl/IWMReader::Close
ms.topic: method
f1_keywords: 
 - "wmsdkidl/IWMReader.Close"
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
 - IWMReader.Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader::Close


## -description



The <b>Close</b> method deletes all outputs on the reader and releases the file resources.




## -parameters






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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The file is already closed

</td>
</tr>
</table>
 




## -remarks



This method sends a WMT_CLOSE status notification to the application's <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-pause">IWMReader::Pause</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-stop">IWMReader::Stop</a>
 

 

