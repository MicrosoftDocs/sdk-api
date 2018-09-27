---
UID: NF:strmif.IAsyncReader.SyncRead
title: IAsyncReader::SyncRead
author: windows-sdk-content
description: The SyncRead method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address do not have to be aligned. If the request is not aligned, the method performs a buffered read operation.
old-location: dshow\iasyncreader_syncread.htm
tech.root: DirectShow
ms.assetid: 21806449-97b1-4890-9182-a1244c21ba30
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAsyncReader interface [DirectShow],SyncRead method, IAsyncReader.SyncRead, IAsyncReader::SyncRead, IAsyncReaderSyncRead, SyncRead, SyncRead method [DirectShow], SyncRead method [DirectShow],IAsyncReader interface, dshow.iasyncreader_syncread, strmif/IAsyncReader::SyncRead
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAsyncReader.SyncRead
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncReader::SyncRead


## -description



The <code>SyncRead</code> method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address do not have to be aligned. If the request is not aligned, the method performs a buffered read operation.




## -parameters




### -param llPosition [in]

Specifies the byte offset at which to begin reading. The method fails if this value is beyond the end of the file.


### -param lLength [in]

Specifies the number of bytes to read.


### -param pBuffer [out]

Pointer to a buffer that receives the data.


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



This method works even if the filter is stopped.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>



<a href="https://msdn.microsoft.com/862511f1-7580-44db-aed5-3dd8279dcc33">IAsyncReader::SyncReadAligned</a>
 

 

