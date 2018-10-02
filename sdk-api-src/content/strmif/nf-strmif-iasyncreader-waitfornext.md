---
UID: NF:strmif.IAsyncReader.WaitForNext
title: IAsyncReader::WaitForNext
author: windows-sdk-content
description: The WaitForNext method waits for the next pending read request to complete.
old-location: dshow\iasyncreader_waitfornext.htm
tech.root: DirectShow
ms.assetid: fc54f917-3b86-4c0b-b356-217bc9793504
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAsyncReader interface [DirectShow],WaitForNext method, IAsyncReader.WaitForNext, IAsyncReader::WaitForNext, IAsyncReaderWaitForNext, WaitForNext, WaitForNext method [DirectShow], WaitForNext method [DirectShow],IAsyncReader interface, dshow.iasyncreader_waitfornext, strmif/IAsyncReader::WaitForNext
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
 - IAsyncReader.WaitForNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncReader::WaitForNext


## -description



The <code>WaitForNext</code> method waits for the next pending read request to complete.




## -parameters




### -param dwTimeout [in]

Specifies a time-out in milliseconds. Use the value INFINITE to wait indefinitely


### -param ppSample [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface pointer.


### -param pdwUser [out]

Pointer to a variable that receives the value of the <i>dwUser</i> parameter specified in the <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a> method.


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
<dt><b>VFW_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out expired, or the pin is flushing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is flushing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A read error occurred.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the file; retrieved fewer bytes than requested.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the <i>ppSample</i> parameter contains a pointer to a media sample, whose buffer holds the requested data. Call the <a href="https://msdn.microsoft.com/f5e95ef3-a101-41c4-8947-f099fcd2490e">IMediaSample::GetTime</a> method and divide the results by 10,000,000 to determine the start and stop bytes. Samples may be returned out of order. Release the sample when you are finished processing the data.

The method fails if the pin is flushing. However, it may return an empty sample in <i>ppSample</i>. If <i>*ppSample</i> is non-<b>NULL</b>, release the sample and discard it. For more information, see <a href="https://msdn.microsoft.com/29153592-dbc1-42b4-bd4e-2f1aef8d4c19">IAsyncReader::BeginFlush</a>.

If a read error occurs, the source filter sends an error event to the Filter Graph Manager; the caller does not have to signal an error.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 

