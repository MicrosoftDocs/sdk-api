---
UID: NF:strmif.IAMStreamSelect.Enable
title: IAMStreamSelect::Enable
author: windows-sdk-content
description: The Enable method enables or disables a given stream.
old-location: dshow\iamstreamselect_enable.htm
tech.root: DirectShow
ms.assetid: ac17a218-34a4-49aa-9b4d-cb34f3c2a5d3
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: Enable, Enable method [DirectShow], Enable method [DirectShow],IAMStreamSelect interface, IAMStreamSelect interface [DirectShow],Enable method, IAMStreamSelect.Enable, IAMStreamSelect::Enable, IAMStreamSelectEnable, dshow.iamstreamselect_enable, strmif/IAMStreamSelect::Enable
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
 - IAMStreamSelect.Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStreamSelect::Enable


## -description



The <code>Enable</code> method enables or disables a given stream.




## -parameters




### -param lIndex [in]

Zero-based index of the stream.


### -param dwFlags [in]

Flag indicating whether to enable or disable the stream. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Disable all streams in the group containing this stream.</td>
</tr>
<tr>
<td>AMSTREAMSELECTENABLE_ENABLE</td>
<td>Enable only this stream within the given group and disable all others.</td>
</tr>
<tr>
<td>AMSTREAMSELECTENABLE_ENABLEALL</td>
<td>Enable all streams in the group containing this stream.</td>
</tr>
</table>
 


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
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The filter does not support the specified flag.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pins are not connected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a305e91e-f506-4bd1-b4d4-7361df89e158">IAMStreamSelect Interface</a>
 

 

