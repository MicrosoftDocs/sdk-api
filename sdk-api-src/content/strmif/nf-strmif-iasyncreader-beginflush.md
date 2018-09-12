---
UID: NF:strmif.IAsyncReader.BeginFlush
title: IAsyncReader::BeginFlush
author: windows-sdk-content
description: The BeginFlush method begins a flush operation.
old-location: dshow\iasyncreader_beginflush.htm
tech.root: DirectShow
ms.assetid: 29153592-dbc1-42b4-bd4e-2f1aef8d4c19
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: BeginFlush, BeginFlush method [DirectShow], BeginFlush method [DirectShow],IAsyncReader interface, IAsyncReader interface [DirectShow],BeginFlush method, IAsyncReader.BeginFlush, IAsyncReader::BeginFlush, IAsyncReaderBeginFlush, dshow.iasyncreader_beginflush, strmif/IAsyncReader::BeginFlush
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
 - IAsyncReader.BeginFlush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncReader::BeginFlush


## -description



The <code>BeginFlush</code> method begins a flush operation.




## -parameters






## -returns



Returns S_OK if successful, or S_FALSE otherwise.




## -remarks



This method interrupts all pending read requests. While the pin is flushing, the <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a> method fails and the <a href="https://msdn.microsoft.com/fc54f917-3b86-4c0b-b356-217bc9793504">IAsyncReader::WaitForNext</a> method returns immediately, possibly with the return code VFW_E_TIMEOUT.

The downstream input pin should call this method whenever the downstream filter flushes the filter graph. After calling this method, call the <b>WaitForNext</b> method until it returns <b>NULL</b> in the <i>ppSample</i> parameter, to clear out the queue of pending samples. Ignore error codes, and release each sample. Then call the <a href="https://msdn.microsoft.com/38a7fd8a-c027-49fd-8f52-49ddf072fe02">IAsyncReader::EndFlush</a> method to end the flush operation.

For more information, see <a href="https://msdn.microsoft.com/868218c4-3e1a-4da0-89fa-30a9848da0e8">Flushing</a>.


#### Examples

The following example shows how a downstream input pin should call this method:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
m_pReader-&gt;BeginFlush(); 
while (1) {
    IMediaSample *pSample;
    DWORD_PTR dwUnused;
    m_pReader-&gt;WaitForNext(0, &amp;pSample, &amp;dwUnused);
    if(pSample) { 
        pSample-&gt;Release();  
    } 
    else {  // No more samples.
        break;
    }
}
m_pReader-&gt;EndFlush();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 

