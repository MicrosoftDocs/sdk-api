---
UID: NF:wmsdkidl.IWMWriterFileSink3.SetAutoIndexing
title: IWMWriterFileSink3::SetAutoIndexing
author: windows-sdk-content
description: The SetAutoIndexing method enables or disables automatic indexing of the file.
old-location: wmformat\iwmwriterfilesink3_setautoindexing.htm
old-project: wmformat
ms.assetid: 6c8f1c25-d752-42b6-87b7-9d6a6e38642f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMWriterFileSink3 interface [windows Media Format],SetAutoIndexing method, IWMWriterFileSink3.SetAutoIndexing, IWMWriterFileSink3::SetAutoIndexing, IWMWriterFileSink3SetAutoIndexing, SetAutoIndexing, SetAutoIndexing method [windows Media Format], SetAutoIndexing method [windows Media Format],IWMWriterFileSink3 interface, wmformat.iwmwriterfilesink3_setautoindexing, wmsdkidl/IWMWriterFileSink3::SetAutoIndexing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterFileSink3.SetAutoIndexing
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink3::SetAutoIndexing


## -description



The <b>SetAutoIndexing</b> method enables or disables automatic indexing of the file.




## -parameters




### -param fDoAutoIndexing [in]

Boolean value that is True to automatically index the file.


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
The header has already been received

</td>
</tr>
</table>
 




## -remarks



The state of automatic indexing must be set before the header is processed. After the header has been processed, any call to <b>SetAutoIndexing</b> results in an error.

Files are indexed by default. To disable indexing, you must call this method, passing False as the parameter.

If you generate an ASF file using bit-rate mutual exclusion for audio content (multiple bit-rate audio), the resulting indexed file will not work with Windows Media Services version 4.1. If you want to stream your file using Windows Media Services 4.1, you must disable automatic indexing before writing the file.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/a6412ce4-03ac-4777-8eb2-ef9f265a6d6c">IWMWriterFileSink3::GetAutoIndexing</a>



<a href="https://msdn.microsoft.com/7daa4b29-0597-462d-ad65-135d0ef7362d">Working with Indexes</a>
 

 

