---
UID: NF:strmif.IAMExtTransport.put_Mode
title: IAMExtTransport::put_Mode
author: windows-sdk-content
description: The put_Mode method sets the transport mode; for example, play, stop, or record.
old-location: dshow\iamexttransport_put_mode.htm
tech.root: DirectShow
ms.assetid: cf941c07-6f42-4c63-9bdf-923f7a5b0b02
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_Mode method, IAMExtTransport.put_Mode, IAMExtTransport::put_Mode, IAMExtTransportput_Mode, dshow.iamexttransport_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_Mode
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
 - IAMExtTransport.put_Mode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::put_Mode


## -description



The <b>put_Mode</b> method sets the transport mode; for example, play, stop, or record.




## -parameters




### -param Mode [in]

Specifies the transport mode. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_MODE_PLAY</td>
<td>Play.</td>
</tr>
<tr>
<td>ED_MODE_STOP</td>
<td>Stop.</td>
</tr>
<tr>
<td>ED_MODE_FREEZE</td>
<td>Pause.</td>
</tr>
<tr>
<td>ED_MODE_THAW</td>
<td>Resume.</td>
</tr>
<tr>
<td>ED_MODE_FF</td>
<td>Fast forward.</td>
</tr>
<tr>
<td>ED_MODE_REW</td>
<td>Rewind.</td>
</tr>
<tr>
<td>ED_MODE_RECORD</td>
<td>Record.</td>
</tr>
<tr>
<td>ED_MODE_RECORD_FREEZE</td>
<td>Pause recording.</td>
</tr>
<tr>
<td>ED_MODE_RECORD_STROBE</td>
<td>Record single frame.</td>
</tr>
<tr>
<td>ED_MODE_STEP_FWD</td>
<td>Single step forward.</td>
</tr>
<tr>
<td>ED_MODE_STEP_REV</td>
<td>Single step backward.</td>
</tr>
<tr>
<td>ED_MODE_SHUTTLE</td>
<td>Shuttle (high-speed movement with visible picture). Use with <a href="https://msdn.microsoft.com/165966f1-f826-4ce2-b520-4a420898eee4">IAMExtTransport::put_Rate</a> to set the transport speed.</td>
</tr>
<tr>
<td>ED_MODE_EDIT_CUE</td>
<td>Position transport to the cue point for an active edit event.</td>
</tr>
<tr>
<td>ED_MODE_LINK_ON</td>
<td>Link this method to the graph's <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a>, <a href="https://msdn.microsoft.com/89e48d43-a31f-4912-98ff-36ba2069812d">IMediaControl::Stop</a>, and <a href="https://msdn.microsoft.com/cfb875b7-cc4e-4ae2-8379-964d0e3ceb04">IMediaControl::Pause</a> methods.</td>
</tr>
<tr>
<td>ED_MODE_LINK_OFF</td>
<td>Disengage this method from the graph's <b>IMediaControl</b> methods.</td>
</tr>
</table>
 


## -returns



Returns an HRESULT. Possible errors include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_REQ_NOT_ACCEP)</b></dt>
</dl>
</td>
<td width="60%">
The device did not accept the command.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/ee08cca0-a2ea-4a7c-8714-f22d5cd62fe8">IAMExtTransport::get_Mode</a>
 

 

