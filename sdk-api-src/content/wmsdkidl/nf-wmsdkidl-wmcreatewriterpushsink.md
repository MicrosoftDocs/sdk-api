---
UID: NF:wmsdkidl.WMCreateWriterPushSink
title: WMCreateWriterPushSink function
author: windows-sdk-content
description: The WMCreateWriterPushSink function creates a writer push sink object. Push sinks are used to deliver streaming content to other media servers for distribution.
old-location: wmformat\wmcreatewriterpushsink.htm
old-project: wmformat
ms.assetid: 544aa6d4-a8fe-4ce5-b329-01b031aa3e6f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WMCreateWriterPushSink, WMCreateWriterPushSink function [windows Media Format], wmformat.wmcreatewriterpushsink, wmsdkidl/WMCreateWriterPushSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateWriterPushSink
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateWriterPushSink function


## -description



The <b>WMCreateWriterPushSink</b> function creates a writer push sink object. Push sinks are used to deliver streaming content to other media servers for distribution.




## -parameters




### -param ppSink [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/47bee154-0d29-4f4c-ac38-af8747088024">IWMWriterPushSink</a> interface of the newly created writer push sink object.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/34e48f35-13d7-4649-a8b2-ed6510b16f88">Writer Push Sink Object</a>
 

 

