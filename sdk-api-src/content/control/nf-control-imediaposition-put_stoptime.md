---
UID: NF:control.IMediaPosition.put_StopTime
title: IMediaPosition::put_StopTime
author: windows-sdk-content
description: The put_StopTime method sets the time at which the playback will stop, relative to the duration of the stream.
old-location: dshow\imediaposition_put_stoptime.htm
tech.root: DirectShow
ms.assetid: c068310e-4083-46ac-8ec6-3d57976f4a88
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMediaPosition interface [DirectShow],put_StopTime method, IMediaPosition.put_StopTime, IMediaPosition::put_StopTime, IMediaPositionput_StopTime, control/IMediaPosition::put_StopTime, dshow.imediaposition_put_stoptime, put_StopTime, put_StopTime method [DirectShow], put_StopTime method [DirectShow],IMediaPosition interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
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
 - IMediaPosition.put_StopTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaPosition::put_StopTime


## -description



The <code>put_StopTime</code> method sets the time at which the playback will stop, relative to the duration of the stream.




## -parameters




### -param llTime [in]

Stop time, in seconds.


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



The stop time ignores the start time and the playback rate. For example, if the start time is 2 seconds, the stop time is 12 seconds, and the playback rate is 2.0, playback will stop after 5 seconds (real time).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 

