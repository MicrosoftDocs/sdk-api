---
UID: NF:strmif.IAMTimecodeReader.GetTCRMode
title: IAMTimecodeReader::GetTCRMode
author: windows-driver-content
description: The GetTCRMode method retrieves the timecode reader's properties.
old-location: dshow\iamtimecodereader_gettcrmode.htm
old-project: DirectShow
ms.assetid: 227c5d8e-fbaf-4bf8-a8c8-954e14e51a24
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetTCRMode, GetTCRMode method [DirectShow], GetTCRMode method [DirectShow],IAMTimecodeReader interface, IAMTimecodeReader interface [DirectShow],GetTCRMode method, IAMTimecodeReader.GetTCRMode, IAMTimecodeReader::GetTCRMode, IAMTimecodeReaderGetTCRMode, dshow.iamtimecodereader_gettcrmode, strmif/IAMTimecodeReader::GetTCRMode
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTimecodeReader.GetTCRMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeReader::GetTCRMode


## -description



The <code>GetTCRMode</code> method retrieves the timecode reader's properties.



This method is not implemented.


## -parameters




### -param Param [in]

Timecode reader property to get (either ED_TCR_SOURCE or ED_TCR_NOTIFY_ENABLE).


### -param pValue [out]

Pointer to the value of the requested timecode reader property. If <i>Param</i> is set to ED_TCR_NOTIFY_ENABLE, then this parameter will return OATRUE—meaning that notifications are enabled—or OAFALSE. If <i>Param</i> is set to ED_TCR_SOURCE, then this value must be one of the following.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ED_TCR_CT</td>
<td>Control track</td>
</tr>
<tr>
<td>ED_TCR_LTC</td>
<td>Linear timecode</td>
</tr>
<tr>
<td>ED_TCR_VITC</td>
<td>Vertical interval timecode</td>
</tr>
<tr>
<td>ED_TCR_LAST_VALUE</td>
<td>Last read value</td>
</tr>
</table>
 


## -returns



Returns E_NOTIMPL.




## -remarks



Linear timecode is recorded on an analog audio track as a bi-phase mark -encoded signal. Each timecode frame is one video frame time in duration.

Vertical timecode is usually stored in two lines of a video signal's vertical interval, somewhere between lines 11 and 20.

Control track is a once-per-frame signal recorded on a special track on a tape. The head and drive servo mechanisms use it to keep everything locked. It is also used to drive the counter on machines without timecode capability, and can optionally be used on machines equipped with a timecode reader.

Note that ED_TCR_LAST_VALUE is used when implementing timecode notification because the application does not want to initiate another timecode request to the external device. This method is not recommended for frame-accurate applications because of multithreading issues.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>



<a href="https://msdn.microsoft.com/dd9f5310-b1c0-46ff-b038-d6a50ac400a2">IAMTimecodeReader::SetTCRMode</a>
 

 

