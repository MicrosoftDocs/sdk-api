---
UID: NE:strmif.__MIDL___MIDL_itf_strmif_0000_0132_0003
title: "__MIDL___MIDL_itf_strmif_0000_0132_0003"
author: windows-sdk-content
description: The DVD_OPTION_FLAG enumeration defines flags that control the behavior of the DVD Navigator Filter. To set any of these flags, call IDvdControl2::SetOption.
old-location: dshow\dvd_option_flag.htm
old-project: DirectShow
ms.assetid: 29e75f58-58f3-4b3f-a3ba-e3451d3a0cae
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DVD_AudioDuringFFwdRew, DVD_CacheSizeInMB, DVD_DisableStillThrottle, DVD_EnableESOutput, DVD_EnableExtendedCopyProtectErrors, DVD_EnableLoggingEvents, DVD_EnableNonblockingAPIs, DVD_EnablePortableBookmarks, DVD_EnableStreaming, DVD_EnableTitleLength, DVD_HMSF_TimeCodeEvents, DVD_IncreaseOutputControl, DVD_MaxReadBurstInKB, DVD_NotifyParentalLevelChange, DVD_NotifyPositionChange, DVD_OPTION_FLAG, DVD_OPTION_FLAG , DVD_OPTION_FLAG enumeration [DirectShow], DVD_OPTION_FLAGEnumeration, DVD_ReadBurstPeriodInMS, DVD_ResetOnStop, __MIDL___MIDL_itf_strmif_0000_0132_0003, dshow.dvd_option_flag, strmif/DVD_AudioDuringFFwdRew, strmif/DVD_CacheSizeInMB, strmif/DVD_DisableStillThrottle, strmif/DVD_EnableESOutput, strmif/DVD_EnableExtendedCopyProtectErrors, strmif/DVD_EnableLoggingEvents, strmif/DVD_EnableNonblockingAPIs, strmif/DVD_EnablePortableBookmarks, strmif/DVD_EnableStreaming, strmif/DVD_EnableTitleLength, strmif/DVD_HMSF_TimeCodeEvents, strmif/DVD_IncreaseOutputControl, strmif/DVD_MaxReadBurstInKB, strmif/DVD_NotifyParentalLevelChange, strmif/DVD_NotifyPositionChange, strmif/DVD_OPTION_FLAG, strmif/DVD_ReadBurstPeriodInMS, strmif/DVD_ResetOnStop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: DVD_OPTION_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_OPTION_FLAG
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# __MIDL___MIDL_itf_strmif_0000_0132_0003 enumeration


## -description



The <b>DVD_OPTION_FLAG</b> enumeration defines flags that control the behavior of the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a>. To set any of these flags, call <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">IDvdControl2::SetOption</a>.




## -enum-fields




### -field DVD_ResetOnStop

Specifies whether the DVD Navigator returns to the start of the disc when the graph stops. 


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The DVD Navigator enters the DVD Stop domain when the filter graph stops. When playback resumes, it starts at the beginning of the disc. </td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The DVD Navigator does not enter the DVD Stop domain when the filter graph stops. When the filter graph starts again, playback resumes from the point where it stopped.</td>
</tr>
</table>
 



The default value is <b>TRUE</b>.

The default behavior is not always desirable, because the filter graph might be stopped unexpectedly. This can happen, for example, if the screen resolution changes, a screen saver starts, or the computer goes into suspended mode. In these situations, the user probably wants playback to restart from the same point. Typically, the application should set this flag to <b>FALSE</b> immediately before calling <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a>. It should set the flag to <b>TRUE</b> before calling <a href="https://msdn.microsoft.com/89e48d43-a31f-4912-98ff-36ba2069812d">IMediaControl::Stop</a> in response to an explicit user to command to stop playback.


### -field DVD_NotifyParentalLevelChange

Specifies whether the DVD Navigator notifies the application when the parental level changes on the disc.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>If the DVD Navigator reaches a temporary parental management level command, it sends the application an <a href="https://msdn.microsoft.com/c6817e1a-f860-4ba2-9e0f-e195624230c5">EC_DVD_PARENTAL_LEVEL_CHANGE</a> event. It blocks playback until it the application responds by calling <a href="https://msdn.microsoft.com/a990544e-6600-44b1-91f2-8b88fa43ccaf">IDvdControl2::AcceptParentalLevelChange</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>When the DVD Navigator encounters a temporary parental management level command and the current parental level is too low, the Navigator automatically rejects the command and branches to whatever path the disc specifies. The Navigator sends an <a href="https://msdn.microsoft.com/c6817e1a-f860-4ba2-9e0f-e195624230c5">EC_DVD_PARENTAL_LEVEL_CHANGE</a> event indicating the required level. The application can stop playback, put up a password dialog box, and restart playback so that it can succeed on the next attempt.</td>
</tr>
</table>
 



The default value <b>FALSE</b>.


### -field DVD_HMSF_TimeCodeEvents

Specifies the format for timecode information.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The DVD Navigator sends all timecode information using the <a href="https://msdn.microsoft.com/8f2990f6-a8f5-4b16-ae30-d51ea55496ea">DVD_HMSF_TIMECODE</a> structure.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The DVD Navigator sends timecode information using binary coded decimal (BCD) format, which is defined in the <a href="https://msdn.microsoft.com/7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4">DVD_TIMECODE</a> structure. </td>
</tr>
</table>
 



For backward compatibility, the default value is <b>FALSE</b>, but the <a href="https://msdn.microsoft.com/8f2990f6-a8f5-4b16-ae30-d51ea55496ea">DVD_HMSF_TIMECODE</a> format is easier to use.


### -field DVD_AudioDuringFFwdRew

Specifies the format for timecode information.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The DVD Navigator enables audio during fast forward and rewind, as long as the audio rate does not exceed the maximum rate of the audio decoder. </td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The Navigator disables audio during fast forward and rewind. </td>
</tr>
</table>
 



The default value is <b>FALS</b>E.

You can also enable audio during fast forward and rewind by creating the following key in the Windows registry:

<code>DWORD HKLM\Software\Microsoft\DVDNavigator\AudioDuringFFwdRev = 1</code>

This has the same effect as setting the DVD_AudioDuringFFwdRew flag to <b>TRUE</b>.


### -field DVD_EnableNonblockingAPIs


<div class="alert"><b>Note</b>  Requires Windows XP Service Pack 2 or later.
            </div>
<div> </div>


If this flag is <b>FALSE</b>, certain DVD Navigator functions block until the DVD Navigator can complete the operation. This is the default behavior.

If this flag is <b>TRUE</b>, those functions no longer block. Instead, if the DVD Navigator cannot complete the operation immediately, the function returns <b>VFW_E_DVD_NONBLOCKING</b>. If the application sets this flag to <b>TRUE</b>, it must handle the <b>VFW_E_DVD_NONBLOCKING</b> error code. Usually the correct behavior is to poll the function until the function succeeds or returns some other error code.

This flag affects at least the following methods: <a href="https://msdn.microsoft.com/ff9eb02c-09c0-4b58-8e38-ec84ab1f1c42">IDvdControl2::ActivateAtPosition</a>, <a href="https://msdn.microsoft.com/f6cb9cb4-0792-43f5-b53b-02a38ccf0398">IDvdControl2::SelectAtPosition</a>, <a href="https://msdn.microsoft.com/54005c07-1689-411c-88a9-bcd19cc065dd">IDvdInfo2::GetCurrentLocation</a>, <a href="https://msdn.microsoft.com/403add2b-3dfd-436d-8184-7a14f30f6ea3">IDvdInfo2::GetState</a>. This list may be expanded in the future.


### -field DVD_CacheSizeInMB


<div class="alert"><b>Note</b>  Requires Windows Vista or later.</div>
<div> </div>


Specifies how much data the DVD Navigator reads in advance, in MB. For this flag, the <i>bEnable</i> parameter of <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">SetOption</a> is interpreted as a <b>DWORD</b> value, rather than a Boolean.

If the application sets this flag to a large value (&gt; 50 MB), the DVD drive may spin down after the initial pre-fetch, depending on the hardware.

You can also set the cache size by creating the following registry key: <code>HKLM\Software\Microsoft\DVDNavigator\CacheSizeInMB</code>. This registry key is intended for diagnostic purposes only. Applications should use the <b>DVD_CacheSizeInMB</b> flag, not the registry key.


### -field DVD_EnablePortableBookmarks


<div class="alert"><b>Note</b>  Requires Windows Vista or later.
            </div>
<div> </div>



<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>DVD bookmarks can be used on another computer. See <a href="https://msdn.microsoft.com/65180fe2-0faf-47c0-bccd-728e01056c46">Saving and Restoring DvdState Objects</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>DVD bookmarks are usable only on the computer where they were created.</td>
</tr>
</table>
 



The default value is <b>FALSE</b>.


### -field DVD_EnableExtendedCopyProtectErrors


<div class="alert"><b>Note</b>  Requires Windows Vista or later.
            </div>
<div> </div>


If this flag <b>TRUE</b>, the DVD Navigator supports an extended set of errors related to copy protection failures. These errors are conveyed through the <a href="https://msdn.microsoft.com/2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a">EC_DVD_ERROR</a> event, and include the following:

<ul>
<li>DVD_PB_STOPPED_CopyProtectOutputNotSupported</li>
<li>DVD_PB_STOPPED_CopyProtectOutputFailure</li>
</ul>
(See <a href="https://msdn.microsoft.com/7f095629-9d44-4666-b14a-932122959f4e">DVD_PB_STOPPED</a>.)

If this flag is <b>FALSE</b>, all copy protection errors are reported using the general <b>DVD_PB_STOPPED_CopyProtectFailure</b> error code.

For backward compatibility, the default value is <b>FALSE</b>.


### -field DVD_NotifyPositionChange


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


If this flag is <b>TRUE</b>, the following events are enabled:

<ul>
<li>
<a href="https://msdn.microsoft.com/a500e86d-cd42-4716-9c57-828a72c4e1df">EC_DVD_PROGRAM_CELL_CHANGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/80fcd059-6ab4-4116-ac3a-012c451237b3">EC_DVD_PROGRAM_CHAIN_CHANGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b8849c8-c71e-44d6-b33a-8e80247bdb22">EC_DVD_TITLE_SET_CHANGE</a>
</li>
</ul>
The default value for this flag is <b>FALSE</b>.


### -field DVD_IncreaseOutputControl


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


Bitwise <b>OR</b> of the following flags:


<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>0x01</td>
<td>Enforce High-Bandwidth Digital Content Protection (HDCP) without fallback.</td>
</tr>
<tr>
<td>0x02</td>
<td>Enforce HDCP even for DVD discs that do not have Content Scramble System (CSS) protection.</td>
</tr>
</table>
 



The default value is zero. These flags are intended for purposes. The recommended value is zero.


### -field DVD_EnableStreaming


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


Enables or disables <i>streaming mode</i>. In streaming mode, bad blocks on the disc are skipped. The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> receives partially corrected data. This mode generally produces better results when playing scratched or damaged disks, because it results in brief video corruption, rather than long waits that block playback. The DVD drive must support streaming I/O.

The default value is <b>TRUE</b>.


### -field DVD_EnableESOutput


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


Enables the <a href="https://msdn.microsoft.com/14f9cfa3-5ef6-419c-9196-2e4060549c03">DVD Navigator</a> to output elementary streams. For more information, see the media types listed in the topic <a href="https://msdn.microsoft.com/14f9cfa3-5ef6-419c-9196-2e4060549c03">DVD Navigator Filter</a>.

The default value is <b>FALSE</b>.


### -field DVD_EnableTitleLength

<i></i>


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>



<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a> method returns the length of the title in the <a href="https://msdn.microsoft.com/e80baf09-93b7-4285-ac9a-af72cae137de">DVD_TitleAttributes</a> structure.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">GetTitleAttributes</a> method returns the title mode (karaoke mode or other mode) and not the title length.</td>
</tr>
</table>
 



The default value is <b>FALSE</b>.


### -field DVD_DisableStillThrottle

If this flag is <b>TRUE</b>, it disables a call to <code>Sleep(1)</code> that the Navigator otherwise makes when displaying stills.

For backward compatibility, the default value for this flag is <b>FALSE</b>, but the recommended value is <b>TRUE</b>.


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>



### -field DVD_EnableLoggingEvents


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


If this flag is <b>TRUE</b>, the following events are enabled:

<ul>
<li>
<a href="https://msdn.microsoft.com/9cdcb211-a9e3-4a15-81bd-7ada2b9d823a">EC_DVD_BeginNavigationCommands</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3e0c400e-9ea5-458c-9eca-97d66a440590">EC_DVD_GPRM_Change</a>
</li>
<li>
<a href="https://msdn.microsoft.com/95e502b6-330f-4bc7-8adc-851913987370">EC_DVD_NavigationCommand</a>
</li>
<li>
<a href="https://msdn.microsoft.com/266b6de1-740d-4b3d-8487-5a9570d6c852">EC_DVD_SPRM_Change</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e2e65007-7c34-4be4-86b9-9491061891e5">EC_DVD_VOBU_Offset</a>
</li>
<li>
<a href="https://msdn.microsoft.com/25548c23-22f0-47cb-9062-273ad39d3007">EC_DVD_VOBU_Timestamp</a>
</li>
</ul>
The default value for this flag is <b>FALSE</b>.


### -field DVD_MaxReadBurstInKB


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


The maximum amount of data that the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> will read ahead in a single burst, in kilobytes. For this flag, the <i>bEnable</i> parameter of <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">SetOption</a> is interpreted as a <b>DWORD</b> value.

The default value is 128 KB.


### -field DVD_ReadBurstPeriodInMS


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


How often to perform burst reads into the cache, in milliseconds. For this flag, the <i>bEnable</i> parameter of <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">SetOption</a> is interpreted as a <b>DWORD</b> value.

The default value is 250 milliseconds.


### -field DVD_RestartDisc


### -field DVD_EnableCC




## -remarks



The following table lists the default values for the Boolean flags.

<table>
<tr>
<th>
              Flag
            </th>
<th>
              Default value
            </th>
</tr>
<tr>
<td><b>DVD_AudioDuringFFwdRew</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_DisableStillThrottle</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableESOutput</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableExtendedCopyProtectErrors</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableLoggingEvents</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableNonblockingAPIs</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableStreaming</b></td>
<td><b>TRUE</b></td>
</tr>
<tr>
<td><b>DVD_EnablePortableBookmarks</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_EnableTitleLength</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_HMSF_TimeCodeEvents</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_NotifyParentalLevelChange</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_NotifyPositionChange</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DVD_ResetOnStop</b></td>
<td><b>TRUE</b></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">IDvdControl2::SetOption</a>
 

 

