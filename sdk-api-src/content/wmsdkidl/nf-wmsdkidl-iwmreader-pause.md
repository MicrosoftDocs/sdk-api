---
UID: NF:wmsdkidl.IWMReader.Pause
title: IWMReader::Pause method
author: windows-driver-content
description: The Pause method pauses the current read operation.
old-location: wmformat\iwmreader_pause.htm
old-project: wmformat
ms.assetid: 4c9d60df-fa9e-42ac-907a-1958a38e430e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMReader, IWMReader interface [windows Media Format], Pause method, IWMReader::Pause, IWMReaderPause, Pause method [windows Media Format], Pause method [windows Media Format], IWMReader interface, Pause,IWMReader.Pause, wmformat.iwmreader_pause, wmsdkidl/IWMReader::Pause
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReader.Pause
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReader::Pause method


## -description



The <b>Pause</b> method pauses the current read operation.




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
 




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/3f320a0c-8586-4fc2-bd70-06ddda435cb5">IWMReader::Close</a>
 

 

