---
UID: NF:wmsdkidl.IWMWriterFileSink2.IsStopped
title: IWMWriterFileSink2::IsStopped
author: windows-sdk-content
description: The IsStopped method ascertains whether the file sink has stopped writing.
old-location: wmformat\iwmwriterfilesink2_isstopped.htm
tech.root: wmformat
ms.assetid: f1e5790a-3cac-4e0e-8a3f-b21afe2711ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],IsStopped method, IWMWriterFileSink2.IsStopped, IWMWriterFileSink2::IsStopped, IWMWriterFileSink2IsStopped, IsStopped, IsStopped method [windows Media Format], IsStopped method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_isstopped, wmsdkidl/IWMWriterFileSink2::IsStopped
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMWriterFileSink2.IsStopped
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink2::IsStopped


## -description



The <b>IsStopped</b> method ascertains whether the file sink has stopped writing.




## -parameters




### -param pfStopped [out]

Pointer to a Boolean value that is set to True if writing has stopped.


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
The <i>pfStopped</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>
 

 

