---
UID: NF:mediaobj.IMediaObject.GetInputStatus
title: IMediaObject::GetInputStatus
author: windows-sdk-content
description: The GetInputStatus method queries whether an input stream can accept more input data.
old-location: dshow\imediaobject_getinputstatus.htm
tech.root: DirectShow
ms.assetid: 4581307f-cea2-4e88-81a1-972e1998c7a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputStatus, GetInputStatus method [DirectShow], GetInputStatus method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputStatus method, IMediaObject.GetInputStatus, IMediaObject::GetInputStatus, IMediaObjectGetInputStatus, dshow.imediaobject_getinputstatus, mediaobj/IMediaObject::GetInputStatus
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetInputStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObject::GetInputStatus


## -description



The <code>GetInputStatus</code> method queries whether an input stream can accept more input data.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param dwFlags [out]

Pointer to a variable that receives either zero or DMO_INPUT_STATUSF_ACCEPT_DATA.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



If the input stream will accept more data, the method returns the DMO_INPUT_STATUSF_ACCEPT_DATA flag in the <i>dwFlags</i> parameter. Otherwise, it sets this parameter to zero. If the stream will accept more data, the application can call the <a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">IMediaObject::ProcessInput</a> method.

The status of an input stream can change only as the result of one of the following method calls.

<table>
<tr>
<th>Method
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd406944(v=VS.85).aspx">IMediaObject::Discontinuity</a>
</td>
<td>Signals a discontinuity on the specified input stream.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd406945(v=VS.85).aspx">IMediaObject::Flush</a>
</td>
<td>Flushes all internally buffered data.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd406959(v=VS.85).aspx">IMediaObject::ProcessInput</a>
</td>
<td>Delivers a buffer to the specified input stream.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd406960(v=VS.85).aspx">IMediaObject::ProcessOutput</a>
</td>
<td>Generates output from the current input data.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd406926(v=VS.85).aspx">IMediaObject Interface</a>
 

 

