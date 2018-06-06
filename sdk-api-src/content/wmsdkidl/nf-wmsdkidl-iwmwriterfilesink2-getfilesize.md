---
UID: NF:wmsdkidl.IWMWriterFileSink2.GetFileSize
title: IWMWriterFileSink2::GetFileSize
author: windows-sdk-content
description: The GetFileSize method retrieves the size of the file.
old-location: wmformat\iwmwriterfilesink2_getfilesize.htm
old-project: wmformat
ms.assetid: 3a5f0c18-f73a-461e-b3cf-48742e74fed3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetFileSize, GetFileSize method [windows Media Format], GetFileSize method [windows Media Format],IWMWriterFileSink2 interface, IWMWriterFileSink2 interface [windows Media Format],GetFileSize method, IWMWriterFileSink2.GetFileSize, IWMWriterFileSink2::GetFileSize, IWMWriterFileSink2GetFileSize, wmformat.iwmwriterfilesink2_getfilesize, wmsdkidl/IWMWriterFileSink2::GetFileSize
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
 - IWMWriterFileSink2.GetFileSize
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink2::GetFileSize


## -description



The <b>GetFileSize</b> method retrieves the size of the file.




## -parameters




### -param pcbFile [out]

Pointer to a count of the bytes in the file.


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
The <i>pcbFile</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>
 

 

