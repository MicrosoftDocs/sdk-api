---
UID: NF:strmif.IAMTimecodeReader.GetTimecode
title: IAMTimecodeReader::GetTimecode
author: windows-sdk-content
description: The GetTimecode method retrieves the most recent timecode, userbit, and flag values available in the stream.
old-location: dshow\iamtimecodereader_gettimecode.htm
tech.root: DirectShow
ms.assetid: c4ed646f-677e-4703-8197-036636f20561
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetTimecode, GetTimecode method [DirectShow], GetTimecode method [DirectShow],IAMTimecodeReader interface, IAMTimecodeReader interface [DirectShow],GetTimecode method, IAMTimecodeReader.GetTimecode, IAMTimecodeReader::GetTimecode, IAMTimecodeReaderGetTimecode, dshow.iamtimecodereader_gettimecode, strmif/IAMTimecodeReader::GetTimecode
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
 - IAMTimecodeReader.GetTimecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTimecodeReader::GetTimecode


## -description



The <code>GetTimecode</code> method retrieves the most recent timecode, userbit, and flag values available in the stream.




## -parameters




### -param pTimecodeSample [out]

Pointer to a <a href="https://msdn.microsoft.com/7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be">TIMECODE_SAMPLE</a> structure.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Use this method to monitor the timecode and to parse duplicates and discontinuities.

The timecode contains undefined bits, called <i>userbits</i>. Applications can use these bits to store synchronization information or other custom information.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>
The <a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> driver supports reading SMPTE timecode or absolute track numbers (ATN). The <a href="https://msdn.microsoft.com/aa59f322-09b1-4b0a-be6f-d865c20f76e5">MSTape</a> driver supports reading the relative time counter (RTC). To read time information on these devices, do the following:

Set the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be">TIMECODE_SAMPLE</a> structure to one of the following values.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_DEVCAP_TIMECODE_READ</td>
<td>Timecode (DV)</td>
</tr>
<tr>
<td>ED_DEVCAP_ATN_READ</td>
<td>Absolute track number (DV)</td>
</tr>
<tr>
<td>ED_DEVCAP_RTC_READ</td>
<td>Relative time counter (MPEG tape)</td>
</tr>
</table>
 

The <b>timecode</b> member of the <a href="https://msdn.microsoft.com/7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be">TIMECODE_SAMPLE</a> structure is a <a href="https://msdn.microsoft.com/e3d06e0c-a595-4bc3-be62-168bd5122397">TIMECODE</a> structure. Initialize that structure's <b>dwFrames</b> member to zero.

All other structure members are ignored.

When the method returns, the <b>dwFrames</b> member contains the time information, in the following format.

<table>
<tr>
<th>Time Information</th>
<th>Format</th>
</tr>
<tr>
<td>Timecode</td>
<td>Hours, minutes, seconds, and frames, as a binary coded decimal (BCD) value: <i>0xhhmmssff</i>.</td>
</tr>
<tr>
<td>ATN</td>
<td>Track number.</td>
</tr>
<tr>
<td>RTC</td>
<td>Hours, minutes, seconds, and frames, as a BCD value: <i>0xhhmmssff</i>. The most significant bit of the frames byte is a sign bit. If the frame count is not available, the remaining frame bits are set to 0x7F.</td>
</tr>
</table>
 

Also, the <b>dwUser</b> member receives the <i>blank flag</i> bit from the device, which has one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0x00</td>
<td>Not a discontinuity.</td>
</tr>
<tr>
<td>0x01</td>
<td>Discontinuity. </td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e3d06e0c-a595-4bc3-be62-168bd5122397">Getting Timecode from the Device</a>



<a href="https://msdn.microsoft.com/76c3f603-8abc-450a-adb2-f2a90cb1634d">IAMTimecodeReader Interface</a>
 

 

