---
UID: NF:strmif.IDvdInfo2.GetAllSPRMs
title: IDvdInfo2::GetAllSPRMs (strmif.h)
description: The GetAllSPRMs method retrieves the current contents of all system parameter registers (SPRMs).
helpviewer_keywords: ["GetAllSPRMs","GetAllSPRMs method [DirectShow]","GetAllSPRMs method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetAllSPRMs method","IDvdInfo2.GetAllSPRMs","IDvdInfo2::GetAllSPRMs","IDvdInfo2GetAllSPRMs","dshow.idvdinfo2_getallsprms","strmif/IDvdInfo2::GetAllSPRMs"]
old-location: dshow\idvdinfo2_getallsprms.htm
tech.root: dshow
ms.assetid: 4a5fb447-670d-4f1f-838e-266843185efe
ms.date: 4/26/2023
ms.keywords: GetAllSPRMs, GetAllSPRMs method [DirectShow], GetAllSPRMs method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetAllSPRMs method, IDvdInfo2.GetAllSPRMs, IDvdInfo2::GetAllSPRMs, IDvdInfo2GetAllSPRMs, dshow.idvdinfo2_getallsprms, strmif/IDvdInfo2::GetAllSPRMs
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetAllSPRMs
 - strmif/IDvdInfo2::GetAllSPRMs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetAllSPRMs
---

# IDvdInfo2::GetAllSPRMs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAllSPRMs</b> method retrieves the current contents of all system parameter registers (SPRMs).

## -parameters

### -param pRegisterArray [out]

Pointer to an array of type <a href="/windows/desktop/DirectShow/sprmarray">SPRMARRAY</a> that receives the address of an array of SPRMs.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

The 24 SPRMs are used to hold information on current language, subpicture, and other navigation data.

<div class="alert"><b>Note</b>  A player application does not need to access these read-only registers for any standard navigation functionality. To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation. The following table lists the contents of each register. Bits within the word are referred to as b0 (low order bit) through b15 (high order bit).</div>
<div> </div>
<table>
<tr>
<th>Register
            </th>
<th>Contents
            </th>
</tr>
<tr>
<td>0</td>
<td>ISO-639 language code (two lowercase ASCII letters). Default value is undefined.</td>
</tr>
<tr>
<td>1</td>
<td>Low 4 bits (b0-b3) contain audio stream number (0 to 7) or 15 (none). Default value is 15.</td>
</tr>
<tr>
<td>2</td>
<td>Low 6 bits (b0-b5) contain subpicture stream number (0 to 31) or 62 (none) or 63 (dummy stream for forced subpicture). 7th bit (b6) contains subpicture display flag (0 = don't display subpicture). Default value is 62.</td>
</tr>
<tr>
<td>3</td>
<td>Low 4 bits (b0-b3) contain angle number (1 to 9). Default value is 1.</td>
</tr>
<tr>
<td>4</td>
<td>Low 7 bits (b0-b6) contain title number (1 to 99). Default value is 1.</td>
</tr>
<tr>
<td>5</td>
<td>Low 7 bits (b0-b6) contain title number within current VTS (1 to 99). Default value is 1.</td>
</tr>
<tr>
<td>6</td>
<td>Low 15 bits (b0-b14) contain PGC number in current title (1 to 32767). Default value is undefined.</td>
</tr>
<tr>
<td>7</td>
<td>Low 10 bits (b0-b9) contain chapter number (1 to 99). Default value is 1. Value undefined unless title is one_sequential_PGC_title.</td>
</tr>
<tr>
<td>8</td>
<td>High 6 bits (b10-b15) contain button number (1 to 36). Default value is 1024 (button 1).</td>
</tr>
<tr>
<td>9</td>
<td>Timer count, in seconds (0 to 65535). Default value is 0.</td>
</tr>
<tr>
<td>10</td>
<td>Low 15 bits (b0-b14) contain PGC number in current title (1 to 32767). Default value is undefined.</td>
</tr>
<tr>
<td>11</td>
<td>Six flags (b2: mix ch2 to ch1, b3: mix ch3 to ch1, b4: mix ch4 to ch1, b10 mix ch2 to ch0, b11: mix ch3 to ch0, b12: mix ch4 to ch0). Flag value of 0 means don't mix. Default value for all flags is 0. Value undefined if not playing Karaoke stream.</td>
</tr>
<tr>
<td>12</td>
<td>ISO-3166 country/region code (two uppercase ASCII letters) or 65535 (not specified). Default value is undefined.</td>
</tr>
<tr>
<td>13</td>
<td>Low 4 bits (b0-b3) contain parental level (1 to 8) or 15 (none). Default value is undefined.</td>
</tr>
<tr>
<td>14</td>
<td>b8-b9 contain current video output mode (0 = normal [4:3 or 16:9], 1 = panscan, 2 = letterbox). b10-b11 contain preferred display mode (0 = 4:3, 3 = 16:9). Default value is undefined.</td>
</tr>
<tr>
<td>15</td>
<td>Nine flags (b2: SDDS karaoke, b3: DTS karaoke, b4: MPEG karaoke, b6: Dolby Digital karaoke, b7: PCM karaoke, b10: SDDS playback, b11: DTS playback, b12: MPEG playback, b14: Dolby Digital playback). Flag value of 0 means incapable, 1 means capable. Default value is undefined.</td>
</tr>
<tr>
<td>16</td>
<td>ISO-639 language code (two lowercase ASCII letters) or 65535 (not specified). Default value is 65535.</td>
</tr>
<tr>
<td>17</td>
<td>Language extension code (0 = not specified, 1 = normal audio, 2 = audio for visually impaired, 3 = director comments #1, 4 = director comments #2). Default value is 0.</td>
</tr>
<tr>
<td>18</td>
<td>ISO-639 language code (two lowercase ASCII letters) or 65535 (not specified). Default value is 65535.</td>
</tr>
<tr>
<td>19</td>
<td>Language extension code (0 = not specified, 1 = normal subtitles, 2 = large subtitles, 3 = subtitles for children, 5 = normal Closed Captions, 6 = large Closed Captions, 7 = Closed Captions for children, 9 = forced subtitles, 13 = director comments, 14 = large director comments, 15 = director comments for children). Default value is 0.</td>
</tr>
<tr>
<td>20</td>
<td>Low 8 bits (b0-b7) contain region code (1 to 8).</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>