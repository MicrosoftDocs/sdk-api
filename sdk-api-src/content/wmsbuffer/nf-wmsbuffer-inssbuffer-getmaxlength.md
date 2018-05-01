---
UID: NF:wmsbuffer.INSSBuffer.GetMaxLength
title: INSSBuffer::GetMaxLength method
author: windows-driver-content
description: The GetMaxLength method retrieves the maximum size to which a buffer can be set.
old-location: wmformat\inssbuffer_getmaxlength.htm
old-project: wmformat
ms.assetid: 6b386c24-1737-4e30-98fa-444fc8a34503
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetMaxLength method [windows Media Format], GetMaxLength method [windows Media Format], INSSBuffer interface, GetMaxLength,INSSBuffer.GetMaxLength, INSSBuffer, INSSBuffer interface [windows Media Format], GetMaxLength method, INSSBuffer::GetMaxLength, INSSBufferGetMaxLength, wmformat.inssbuffer_getmaxlength, wmsbuffer/INSSBuffer::GetMaxLength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsbuffer.h
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
req.typenames: WMPServices_StreamState
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
-	INSSBuffer.GetMaxLength
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# INSSBuffer::GetMaxLength method


## -description



The <b>GetMaxLength</b> method retrieves the maximum size to which a buffer can be set. The maximum value is set when the sample is created. If you are using <a href="https://msdn.microsoft.com/b23b2364-fb36-479f-bf92-76a5bb4722de">IWMWriter::AllocateSample</a>, the size you specify becomes the maximum buffer length. The actual amount of the buffer that is used can be retrieved by calling <a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the maximum length, in bytes.


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
The <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The maximum size of the buffer as returned by this method does not affect or reflect the size of any data unit extensions associated with the sample stored in the buffer.




## -see-also




<a href="https://msdn.microsoft.com/f95de189-0449-4b88-aba3-7b19f385c8fe">Data Unit Extensions</a>



<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>
 

 

