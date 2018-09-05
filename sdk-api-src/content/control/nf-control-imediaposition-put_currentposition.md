---
UID: NF:control.IMediaPosition.put_CurrentPosition
title: IMediaPosition::put_CurrentPosition
author: windows-sdk-content
description: The put_CurrentPosition method sets the current position, relative to the total duration of the stream.
old-location: dshow\imediaposition_put_currentposition.htm
old-project: DirectShow
ms.assetid: 6af44ce9-91d3-4329-835a-a1249924d672
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMediaPosition interface [DirectShow],put_CurrentPosition method, IMediaPosition.put_CurrentPosition, IMediaPosition::put_CurrentPosition, IMediaPositionput_CurrentPosition, control/IMediaPosition::put_CurrentPosition, dshow.imediaposition_put_currentposition, put_CurrentPosition, put_CurrentPosition method [DirectShow], put_CurrentPosition method [DirectShow],IMediaPosition interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaPosition.put_CurrentPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaPosition::put_CurrentPosition


## -description



The <code>put_CurrentPosition</code> method sets the current position, relative to the total duration of the stream.




## -parameters




### -param llTime [in]

New position, in seconds.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

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
Graph was paused and is in transition back to a running state.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



The position specified by the <i>llTime</i> parameter is relative to the total duration, ignoring playback rate. For example, if a source file is 10 seconds long, setting the position to 5.0 causes the graph to seek to the middle of the file, regardless of playback rate.

If the filter graph is running, the Filter Graph Manager pauses the graph, issues the seek command, and then runs the graph again. If the method returns while the graph is still transitioning to a running state, the return value is S_FALSE.

If a filter is paused when it receives a seek command, it must flush existing data before it introduces the data from the new position. See <a href="https://msdn.microsoft.com/15563666-5f35-46a0-ad12-215979c9d9c1">IPin::BeginFlush</a> and <a href="https://msdn.microsoft.com/42b201b6-1fbf-4a01-aed7-23a9e66c11ea">IPin::EndFlush</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 

