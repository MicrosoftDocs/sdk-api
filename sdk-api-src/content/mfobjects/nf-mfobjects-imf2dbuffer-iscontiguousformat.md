---
UID: NF:mfobjects.IMF2DBuffer.IsContiguousFormat
title: IMF2DBuffer::IsContiguousFormat (mfobjects.h)
author: windows-sdk-content
description: Queries whether the buffer is contiguous in its native format.
old-location: mf\imf2dbuffer_iscontiguousformat.htm
tech.root: medfound
ms.assetid: a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMF2DBuffer interface [Media Foundation],IsContiguousFormat method, IMF2DBuffer.IsContiguousFormat, IMF2DBuffer::IsContiguousFormat, IsContiguousFormat, IsContiguousFormat method [Media Foundation], IsContiguousFormat method [Media Foundation],IMF2DBuffer interface, a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e, mf.imf2dbuffer_iscontiguousformat, mfobjects/IMF2DBuffer::IsContiguousFormat
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMF2DBuffer.IsContiguousFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMF2DBuffer::IsContiguousFormat


## -description



Queries whether the buffer is contiguous in its native format.




## -parameters




### -param pfIsContiguous [out]

Receives a Boolean value. The value is <b>TRUE</b> if the buffer is contiguous, and <b>FALSE</b> otherwise.


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
</table>
 




## -remarks



For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface. For non-contiguous buffers, the <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a> method must perform an internal copy.




## -see-also




<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/be5ec8a8-2d0b-401b-9d05-fdb87ad8c864">Uncompressed Video Buffers</a>
 

 

