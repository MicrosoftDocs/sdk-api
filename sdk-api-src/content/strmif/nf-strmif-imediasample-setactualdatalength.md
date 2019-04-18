---
UID: NF:strmif.IMediaSample.SetActualDataLength
title: IMediaSample::SetActualDataLength (strmif.h)
author: windows-sdk-content
description: The SetActualDataLength method sets the length of the valid data in the buffer.
old-location: dshow\imediasample_setactualdatalength.htm
tech.root: DirectShow
ms.assetid: db8a768e-7550-4165-8f87-308ec7f2e07f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],SetActualDataLength method, IMediaSample.SetActualDataLength, IMediaSample::SetActualDataLength, IMediaSampleSetActualDataLength, SetActualDataLength, SetActualDataLength method [DirectShow], SetActualDataLength method [DirectShow],IMediaSample interface, dshow.imediasample_setactualdatalength, strmif/IMediaSample::SetActualDataLength
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
 - IMediaSample.SetActualDataLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample::SetActualDataLength


## -description



The <code>SetActualDataLength</code> method sets the length of the valid data in the buffer.




## -parameters




### -param __MIDL__IMediaSample0000

Length of the data in the media sample, in bytes.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>VFW_E_BUFFER_OVERFLOW.</b></dt>
</dl>
</td>
<td width="60%">
Length specified in <i>lLen</i> is larger than the buffer size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

