---
UID: NF:strmif.IAsyncReader.SyncReadAligned
title: IAsyncReader::SyncReadAligned
author: windows-sdk-content
description: The SyncReadAligned method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address must be aligned; check the allocator properties for the required alignment.
old-location: dshow\iasyncreader_syncreadaligned.htm
old-project: DirectShow
ms.assetid: 862511f1-7580-44db-aed5-3dd8279dcc33
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAsyncReader interface [DirectShow],SyncReadAligned method, IAsyncReader.SyncReadAligned, IAsyncReader::SyncReadAligned, IAsyncReaderSyncReadAligned, SyncReadAligned, SyncReadAligned method [DirectShow], SyncReadAligned method [DirectShow],IAsyncReader interface, dshow.iasyncreader_syncreadaligned, strmif/IAsyncReader::SyncReadAligned
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAsyncReader.SyncReadAligned
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAsyncReader::SyncReadAligned


## -description



The <code>SyncReadAligned</code> method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address must be aligned; check the allocator properties for the required alignment.




## -parameters




### -param pSample

Pointer to the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface of a media sample provided by the caller.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
Invalid alignment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Retrieved fewer bytes than requested. (Probably the end of the file was reached.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, retrieve a media sample from the pin's allocator. Time stamp the sample with the byte offsets you are requesting, first and last inclusive, multiplied by 10,000,000. Byte offsets are relative to the start of the stream.

The start and stop positions should match the alignment that was decided when the pins connected. Otherwise, the method returns VFW_E_BADALIGN. If the agreed alignment is coarser than the actual alignment of the stream, the stop position might exceed the real duration. If so, the method rounds the stop position down to the actual alignment.

This method performs an unbuffered read, so it might be faster than the <a href="https://msdn.microsoft.com/21806449-97b1-4890-9182-a1244c21ba30">IAsyncReader::SyncRead</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 

