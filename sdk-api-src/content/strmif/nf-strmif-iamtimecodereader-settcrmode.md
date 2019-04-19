---
UID: NF:strmif.IAMTimecodeReader.SetTCRMode
title: IAMTimecodeReader::SetTCRMode (strmif.h)
author: windows-sdk-content
description: The SetTCRMode method sets the timecode reader properties.
old-location: dshow\iamtimecodereader_settcrmode.htm
tech.root: DirectShow
ms.assetid: dd9f5310-b1c0-46ff-b038-d6a50ac400a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTimecodeReader interface [DirectShow],SetTCRMode method, IAMTimecodeReader.SetTCRMode, IAMTimecodeReader::SetTCRMode, IAMTimecodeReaderSetTCRMode, SetTCRMode, SetTCRMode method [DirectShow], SetTCRMode method [DirectShow],IAMTimecodeReader interface, dshow.iamtimecodereader_settcrmode, strmif/IAMTimecodeReader::SetTCRMode
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
 - IAMTimecodeReader.SetTCRMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeReader::SetTCRMode


## -description



The <code>SetTCRMode</code> method sets the timecode reader properties.



This method is not implemented.


## -parameters




### -param Param [in]

Property you want to set (use ED_TCR_SOURCE or ED_TCR_NOTIFY_ENABLE).


### -param Value [in]

Value of the specified property; If <i>Param</i> returns ED_TCR_NOTIFY_ENABLE, then this value will return OATRUE or OAFALSE. If <i>Param</i> returns ED_TCR_SOURCE, then this value must be one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCR_CT</td>
<td>Control Track.</td>
</tr>
<tr>
<td>ED_TCR_LTC</td>
<td>Linear Timecode.</td>
</tr>
<tr>
<td>ED_TCR_VITC</td>
<td>Vertical Interval Timecode.</td>
</tr>
<tr>
<td>ED_TCR_LAST_VALUE</td>
<td>Return last read value.</td>
</tr>
</table>
 


## -returns



Returns E_NOTIMPL.




## -remarks



Linear timecode is recorded on an analog audio track as an NRZ bi-phase mark-encoded signal. Each timecode frame is one video frame time in duration.

Vertical timecode is usually stored in two lines of a video signal's vertical interval, somewhere between 10 and 20.

Control track is a once-per-frame signal recorded on a special track on a tape. The head and drive servo mechanisms use it to keep everything locked. It is also used to drive the counter on machines without timecode capability, and can optionally be used on machines equipped with a timecode reader.

Note that ED_TCR_LAST_VALUE is used when implementing timecode notification because the application does not want to initiate another timecode request to the external device. This method is not recommended for frame-accurate applications because of multithreading issues.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>



<a href="https://msdn.microsoft.com/227c5d8e-fbaf-4bf8-a8c8-954e14e51a24">IAMTimecodeReader::GetTCRMode</a>
 

 

