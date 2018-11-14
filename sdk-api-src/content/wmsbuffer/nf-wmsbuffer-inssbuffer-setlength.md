---
UID: NF:wmsbuffer.INSSBuffer.SetLength
title: INSSBuffer::SetLength
author: windows-sdk-content
description: The SetLength method specifies the size of the used portion of the buffer.
old-location: wmformat\inssbuffer_setlength.htm
tech.root: wmformat
ms.assetid: 3f0e8d8a-efc7-4f1b-8a42-7907439ed8af
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: INSSBuffer interface [windows Media Format],SetLength method, INSSBuffer.SetLength, INSSBuffer::SetLength, INSSBufferSetLength, SetLength, SetLength method [windows Media Format], SetLength method [windows Media Format],INSSBuffer interface, wmformat.inssbuffer_setlength, wmsbuffer/INSSBuffer::SetLength
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
 - INSSBuffer.SetLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsbuffer.h
: 
- INSSBuffer.SetLength
: 
---

# INSSBuffer::SetLength


## -description



The <b>SetLength</b> method specifies the size of the used portion of the buffer. If you are storing a sample in the buffer, call <a href="https://msdn.microsoft.com/3f9e8408-52ce-48aa-ba85-51bdbbfd8b51">INSSBuffer::GetBuffer</a> to retrieve the address of the buffer. Then copy your data to that address and use this method to set the length of the used portion of the buffer.




## -parameters




### -param dwLength [in]

<b>DWORD</b> containing the size of the used portion, in bytes.


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
<i>dwLength</i> is greater than the buffer size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer Interface</a>



<a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">INSSBuffer::GetLength</a>
 

 

