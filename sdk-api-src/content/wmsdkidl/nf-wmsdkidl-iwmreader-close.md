---
UID: NF:wmsdkidl.IWMReader.Close
title: IWMReader::Close
author: windows-sdk-content
description: The Close method deletes all outputs on the reader and releases the file resources.
old-location: wmformat\iwmreader_close.htm
old-project: wmformat
ms.assetid: 3f320a0c-8586-4fc2-bd70-06ddda435cb5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],Close method, IWMReader.Close, IWMReader::Close, IWMReaderClose, wmformat.iwmreader_close, wmsdkidl/IWMReader::Close
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
 - IWMReader.Close
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



This method sends a WMT_CLOSE status notification to the application's <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>



<a href="https://msdn.microsoft.com/4c9d60df-fa9e-42ac-907a-1958a38e430e">IWMReader::Pause</a>



<a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a>



<a href="https://msdn.microsoft.com/781d1882-4b48-4415-9b3a-788207b42151">IWMReader::Stop</a>
 

 

