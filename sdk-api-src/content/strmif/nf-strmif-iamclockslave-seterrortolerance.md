---
UID: NF:strmif.IAMClockSlave.SetErrorTolerance
title: IAMClockSlave::SetErrorTolerance
author: windows-sdk-content
description: The SetErrorTolerance method sets the audio renderer's rate-matching tolerance.
old-location: dshow\iamclockslave_seterrortolerance.htm
tech.root: DirectShow
ms.assetid: 6c93e345-4e4a-4019-9c18-d3d43736fee3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMClockSlave interface [DirectShow],SetErrorTolerance method, IAMClockSlave.SetErrorTolerance, IAMClockSlave::SetErrorTolerance, IAMClockSlaveSetErrorTolerance, SetErrorTolerance, SetErrorTolerance method [DirectShow], SetErrorTolerance method [DirectShow],IAMClockSlave interface, dshow.iamclockslave_seterrortolerance, strmif/IAMClockSlave::SetErrorTolerance
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMClockSlave.SetErrorTolerance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMClockSlave::SetErrorTolerance


## -description



The <code>SetErrorTolerance</code> method sets the audio renderer's rate-matching tolerance.




## -parameters




### -param dwTolerance [in]

Specifies the maximum tolerance, in milliseconds. The value must be from 1 to 1000, inclusive.


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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>
 




## -remarks



Changing the tolerance has no effect unless the audio renderer is matching rates with a different clock. If the audio renderer is the reference clock, the audio is always synchronized to the clock (by definition).

This method fails if the filter graph is not stopped.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7b3d0f93-09dd-4a36-a031-70f61402c314">IAMClockSlave Interface</a>
 

 

