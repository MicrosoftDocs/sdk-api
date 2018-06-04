---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDvdInfo2::GetAllSPRMs


## -description



The <b>GetAllSPRMs</b> method retrieves the current contents of all system parameter registers (SPRMs).




## -parameters




### -param pRegisterArray [out]


            Pointer to an array of type <a href="https://msdn.microsoft.com/5c285f6e-2921-4684-bc42-762fc80a5e6b">SPRMARRAY</a> that receives the address of an array of SPRMs.
          


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
<th>
              Register
            </th>
<th>
              Contents
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




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

