---
UID: NF:strmif.IAsyncReader.RequestAllocator
title: IAsyncReader::RequestAllocator (strmif.h)
author: windows-sdk-content
description: The RequestAllocator method requests an allocator during the pin connection.
old-location: dshow\iasyncreader_requestallocator.htm
tech.root: DirectShow
ms.assetid: 7bde850e-662f-4610-bac3-914c93584b30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAsyncReader interface [DirectShow],RequestAllocator method, IAsyncReader.RequestAllocator, IAsyncReader::RequestAllocator, IAsyncReaderRequestAllocator, RequestAllocator, RequestAllocator method [DirectShow], RequestAllocator method [DirectShow],IAsyncReader interface, dshow.iasyncreader_requestallocator, strmif/IAsyncReader::RequestAllocator
ms.topic: method
f1_keywords: ["strmif/IAsyncReader.RequestAllocator"]
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
 - IAsyncReader.RequestAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsyncReader::RequestAllocator


## -description



The <code>RequestAllocator</code> method requests an allocator during the pin connection.




## -parameters




### -param pPreferred [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface on the input pin's preferred allocator, or <b>NULL</b>.


### -param pProps [in]

Specifies the address of an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-_allocatorproperties">ALLOCATOR_PROPERTIES</a> structure, allocated by the caller. The caller should fill in any allocator properties that the input pin requires, and set the remaining members to zero.


### -param ppActual [out]

Address of a variable that receives an <b>IMemAllocator</b> interface pointer.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure to initialize an allocator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
An invalid alignment was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Allocator was returned.

</td>
</tr>
</table>
 




## -remarks



The downstream input pin should call this method during the connection process. If the pin has a preferred allocator, specify it in the <i>pPreferred</i> parameter. Specify any buffer requirements, such as buffer size or alignment, in the <i>pProps</i> parameter. The output pin chooses the allocator and returns a pointer to it in the <i>ppActual</i> parameter.

The output pin is not required to honor the input pin's requests. If the input pin has any absolute requirements, it should call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-getproperties">IMemAllocator::GetProperties</a> method on the returned allocator. It can fail the connect if the allocator properties are not suitable. Once the connection is established, the input pin must use the allocator chosen by the output pin.

The input pin is responsible for committing and decommitting the allocator.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>
 

 

