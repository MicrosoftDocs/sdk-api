---
UID: NF:wmsdkidl.WMCreateWriterPushSink
title: WMCreateWriterPushSink function (wmsdkidl.h)
author: windows-sdk-content
description: The WMCreateWriterPushSink function creates a writer push sink object. Push sinks are used to deliver streaming content to other media servers for distribution.
old-location: wmformat\wmcreatewriterpushsink.htm
tech.root: wmformat
ms.assetid: 544aa6d4-a8fe-4ce5-b329-01b031aa3e6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMCreateWriterPushSink, WMCreateWriterPushSink function [windows Media Format], wmformat.wmcreatewriterpushsink, wmsdkidl/WMCreateWriterPushSink
ms.topic: function
f1_keywords: 
 - "wmsdkidl/WMCreateWriterPushSink"
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateWriterPushSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateWriterPushSink function


## -description



The <b>WMCreateWriterPushSink</b> function creates a writer push sink object. Push sinks are used to deliver streaming content to other media servers for distribution.




## -parameters




### -param ppSink [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink">IWMWriterPushSink</a> interface of the newly created writer push sink object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-push-sink-object">Writer Push Sink Object</a>
 

 

