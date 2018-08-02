---
UID: NF:wmsdkidl.IWMWriterFileSink.Open
title: IWMWriterFileSink::Open
author: windows-sdk-content
description: The Open method opens a file that acts as the writer sink.
old-location: wmformat\iwmwriterfilesink_open.htm
old-project: wmformat
ms.assetid: 14a36fe9-8293-4079-8189-8a8e0720c100
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMWriterFileSink interface [windows Media Format],Open method, IWMWriterFileSink.Open, IWMWriterFileSink::Open, IWMWriterFileSinkOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMWriterFileSink interface, wmformat.iwmwriterfilesink_open, wmsdkidl/IWMWriterFileSink::Open
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
 - IWMWriterFileSink.Open
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink::Open


## -description



The <b>Open</b> method opens a file that acts as the writer sink.




## -parameters




### -param pwszFilename [in]

Pointer to a wide-character <b>null</b>-terminated string containing the file name. URLs are not supported.


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
The <i>pwszFilename</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



There is no close method in this interface as the closing of the writer sink file is done automatically by a call to <a href="https://msdn.microsoft.com/020e2c9d-9581-48c9-bc7b-a0e9e5a60c63">IWMWriter::EndWriting</a>.

See the Remarks and Example Code sections for <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>.




## -see-also




<a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink Interface</a>
 

 

