---
UID: NF:wmsdkidl.IWMReader.Stop
title: IWMReader::Stop
author: windows-sdk-content
description: The Stop method stops reading the file.
old-location: wmformat\iwmreader_stop.htm
old-project: wmformat
ms.assetid: 781d1882-4b48-4415-9b3a-788207b42151
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReader interface [windows Media Format],Stop method, IWMReader.Stop, IWMReader::Stop, IWMReaderStop, Stop, Stop method [windows Media Format], Stop method [windows Media Format],IWMReader interface, wmformat.iwmreader_stop, wmsdkidl/IWMReader::Stop
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
 - IWMReader.Stop
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReader::Stop


## -description



The <b>Stop</b> method stops reading the file.




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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



This method sends a WMT_STOPPED status notification to the application's <b>IWMReaderCallback::OnStatus</b> function.

Calling <b>Stop</b> eliminates the current read position. If <b>Start</b> is called with a start time set at WM_START_CURRENTPOSITION after calling <b>Stop</b>, an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/3f320a0c-8586-4fc2-bd70-06ddda435cb5">IWMReader::Close</a>



<a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>



<a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a>



<a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback Interface</a>
 

 

