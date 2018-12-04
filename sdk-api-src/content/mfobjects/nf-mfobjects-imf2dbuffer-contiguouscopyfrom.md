---
UID: NF:mfobjects.IMF2DBuffer.ContiguousCopyFrom
title: IMF2DBuffer::ContiguousCopyFrom
author: windows-sdk-content
description: Copies data to this buffer from a buffer that has a contiguous format.
old-location: mf\imf2dbuffer_contiguouscopyfrom.htm
tech.root: medfound
ms.assetid: 84634782-7805-4e2b-a043-7e49adef5c2a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 84634782-7805-4e2b-a043-7e49adef5c2a, ContiguousCopyFrom, ContiguousCopyFrom method [Media Foundation], ContiguousCopyFrom method [Media Foundation],IMF2DBuffer interface, IMF2DBuffer interface [Media Foundation],ContiguousCopyFrom method, IMF2DBuffer.ContiguousCopyFrom, IMF2DBuffer::ContiguousCopyFrom, mf.imf2dbuffer_contiguouscopyfrom, mfobjects/IMF2DBuffer::ContiguousCopyFrom
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMF2DBuffer.ContiguousCopyFrom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMF2DBuffer::ContiguousCopyFrom


## -description



Copies data to this buffer from a buffer that has a contiguous format.




## -parameters




### -param pbSrcBuffer [in]

Pointer to the source buffer. The caller allocates the buffer.


### -param cbSrcBuffer [in]

Size of the source buffer, in bytes. To get the maximum size of the buffer, call <a href="https://msdn.microsoft.com/413d50f6-a047-4561-985d-9d1927825617">IMF2DBuffer::GetContiguousLength</a>.


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



This method copies the contents of the source buffer into the buffer that is managed by this <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> object. The source buffer must be in contiguous format. While copying, the method converts the contents into the destination buffer's native format, correcting for the buffer's pitch if necessary.

For a definition of contiguous as it applies to 2-D buffers, see the Remarks section in the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface topic.




## -see-also




<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/be5ec8a8-2d0b-401b-9d05-fdb87ad8c864">Uncompressed Video Buffers</a>
 

 

