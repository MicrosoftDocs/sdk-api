---
UID: NF:strmif.IPin.EndFlush
title: IPin::EndFlush
author: windows-sdk-content
description: The EndFlush method ends a flush operation.
old-location: dshow\ipin_endflush.htm
old-project: DirectShow
ms.assetid: 42b201b6-1fbf-4a01-aed7-23a9e66c11ea
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: EndFlush, EndFlush method [DirectShow], EndFlush method [DirectShow],IPin interface, IPin interface [DirectShow],EndFlush method, IPin.EndFlush, IPin::EndFlush, IPinEndFlush, dshow.ipin_endflush, strmif/IPin::EndFlush
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
 - IPin.EndFlush
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::EndFlush


## -description



The <code>EndFlush</code> method ends a flush operation.



Applications should not call this method. This method is called by other filters, to flush data from the graph.


## -parameters






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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is an output pin.

</td>
</tr>
</table>
 




## -remarks



Call this method only on input pins. Output pins return E_UNEXPECTED.

When this method is called, the filter performs the following actions:

<ol>
<li>Waits for all queued samples to be discarded.</li>
<li>Frees any buffered data, including any pending end-of-stream notifications.</li>
<li>Clears any pending <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> notifications.</li>
<li>Calls <code>EndFlush</code> downstream.</li>
</ol>
When the method returns, the pin can accept new samples.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

