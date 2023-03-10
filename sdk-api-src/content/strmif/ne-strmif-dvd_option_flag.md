---
UID: NE:strmif.__MIDL___MIDL_itf_strmif_0000_0132_0003
title: DVD_OPTION_FLAG (strmif.h)
description: The DVD_OPTION_FLAG enumeration defines flags that control the behavior of the DVD Navigator Filter. To set any of these flags, call IDvdControl2::SetOption.
helpviewer_keywords: ["DVD_AudioDuringFFwdRew","DVD_CacheSizeInMB","DVD_DisableStillThrottle","DVD_EnableESOutput","DVD_EnableExtendedCopyProtectErrors","DVD_EnableLoggingEvents","DVD_EnableNonblockingAPIs","DVD_EnablePortableBookmarks","DVD_EnableStreaming","DVD_EnableTitleLength","DVD_HMSF_TimeCodeEvents","DVD_IncreaseOutputControl","DVD_MaxReadBurstInKB","DVD_NotifyParentalLevelChange","DVD_NotifyPositionChange","DVD_OPTION_FLAG","DVD_OPTION_FLAG","DVD_OPTION_FLAG enumeration [DirectShow]","DVD_OPTION_FLAGEnumeration","DVD_ReadBurstPeriodInMS","DVD_ResetOnStop","dshow.dvd_option_flag","strmif/DVD_AudioDuringFFwdRew","strmif/DVD_CacheSizeInMB","strmif/DVD_DisableStillThrottle","strmif/DVD_EnableESOutput","strmif/DVD_EnableExtendedCopyProtectErrors","strmif/DVD_EnableLoggingEvents","strmif/DVD_EnableNonblockingAPIs","strmif/DVD_EnablePortableBookmarks","strmif/DVD_EnableStreaming","strmif/DVD_EnableTitleLength","strmif/DVD_HMSF_TimeCodeEvents","strmif/DVD_IncreaseOutputControl","strmif/DVD_MaxReadBurstInKB","strmif/DVD_NotifyParentalLevelChange","strmif/DVD_NotifyPositionChange","strmif/DVD_OPTION_FLAG","strmif/DVD_ReadBurstPeriodInMS","strmif/DVD_ResetOnStop"]
old-location: dshow\dvd_option_flag.htm
tech.root: dshow
ms.assetid: 29e75f58-58f3-4b3f-a3ba-e3451d3a0cae
ms.date: 12/05/2018
ms.keywords: DVD_AudioDuringFFwdRew, DVD_CacheSizeInMB, DVD_DisableStillThrottle, DVD_EnableESOutput, DVD_EnableExtendedCopyProtectErrors, DVD_EnableLoggingEvents, DVD_EnableNonblockingAPIs, DVD_EnablePortableBookmarks, DVD_EnableStreaming, DVD_EnableTitleLength, DVD_HMSF_TimeCodeEvents, DVD_IncreaseOutputControl, DVD_MaxReadBurstInKB, DVD_NotifyParentalLevelChange, DVD_NotifyPositionChange, DVD_OPTION_FLAG, DVD_OPTION_FLAG , DVD_OPTION_FLAG enumeration [DirectShow], DVD_OPTION_FLAGEnumeration, DVD_ReadBurstPeriodInMS, DVD_ResetOnStop, dshow.dvd_option_flag, strmif/DVD_AudioDuringFFwdRew, strmif/DVD_CacheSizeInMB, strmif/DVD_DisableStillThrottle, strmif/DVD_EnableESOutput, strmif/DVD_EnableExtendedCopyProtectErrors, strmif/DVD_EnableLoggingEvents, strmif/DVD_EnableNonblockingAPIs, strmif/DVD_EnablePortableBookmarks, strmif/DVD_EnableStreaming, strmif/DVD_EnableTitleLength, strmif/DVD_HMSF_TimeCodeEvents, strmif/DVD_IncreaseOutputControl, strmif/DVD_MaxReadBurstInKB, strmif/DVD_NotifyParentalLevelChange, strmif/DVD_NotifyPositionChange, strmif/DVD_OPTION_FLAG, strmif/DVD_ReadBurstPeriodInMS, strmif/DVD_ResetOnStop
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVD_OPTION_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_strmif_0000_0132_0003
 - strmif/__MIDL___MIDL_itf_strmif_0000_0132_0003
 - DVD_OPTION_FLAG
 - strmif/DVD_OPTION_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_OPTION_FLAG
---

# DVD_OPTION_FLAG enumeration


## -description

The <b>DVD_OPTION_FLAG</b> enumeration defines flags that control the behavior of the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a>. To set any of these flags, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a>.

## -enum-fields

### -field DVD_ResetOnStop:1

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

The default behavior is not always desirable, because the filter graph might be stopped unexpectedly. This can happen, for example, if the screen resolution changes, a screen saver starts, or the computer goes into suspended mode. In these situations, the user probably wants playback to restart from the same point. Typically, the application should set this flag to <b>FALSE</b> immediately before calling <a href="/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a>. It should set the flag to <b>TRUE</b> before calling <a href="/windows/desktop/api/control/nf-control-imediacontrol-stop">IMediaControl::Stop</a> in response to an explicit user to command to stop playback.

### -field DVD_NotifyParentalLevelChange:2

Specifies whether the DVD Navigator notifies the application when the parental level changes on the disc.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>If the DVD Navigator reaches a temporary parental management level command, it sends the application an <a href="/windows/desktop/DirectShow/ec-dvd-parental-level-change">EC_DVD_PARENTAL_LEVEL_CHANGE</a> event. It blocks playback until it the application responds by calling <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange">IDvdControl2::AcceptParentalLevelChange</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>When the DVD Navigator encounters a temporary parental management level command and the current parental level is too low, the Navigator automatically rejects the command and branches to whatever path the disc specifies. The Navigator sends an <a href="/windows/desktop/DirectShow/ec-dvd-parental-level-change">EC_DVD_PARENTAL_LEVEL_CHANGE</a> event indicating the required level. The application can stop playback, put up a password dialog box, and restart playback so that it can succeed on the next attempt.</td>
</tr>
</table>
 



The default value <b>FALSE</b>.

### -field DVD_HMSF_TimeCodeEvents:3

Specifies the format for timecode information.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>TRUE</b></td>
[DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) structure.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
[DVD_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_timecode) structure. </td>
</tr>
</table>
 



For backward compatibility, the default value is [DVD_HMSF_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) format is easier to use.

### -field DVD_AudioDuringFFwdRew:4

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
 



The default value is <b>FALSE</b>.

You can also enable audio during fast forward and rewind by creating the following key in the Windows registry:

<code>DWORD HKLM\Software\Microsoft\DVDNavigator\AudioDuringFFwdRev = 1</code>

This has the same effect as setting the DVD_AudioDuringFFwdRew flag to <b>TRUE</b>.

### -field DVD_EnableNonblockingAPIs:5

<div class="alert"><b>Note</b>  Requires Windows XP Service Pack 2 or later.
            </div>
<div> </div>


If this flag is <b>FALSE</b>, certain DVD Navigator functions block until the DVD Navigator can complete the operation. This is the default behavior.

If this flag is <b>TRUE</b>, those functions no longer block. Instead, if the DVD Navigator cannot complete the operation immediately, the function returns <b>VFW_E_DVD_NONBLOCKING</b>. If the application sets this flag to <b>TRUE</b>, it must handle the <b>VFW_E_DVD_NONBLOCKING</b> error code. Usually the correct behavior is to poll the function until the function succeeds or returns some other error code.

This flag affects at least the following methods: <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-activateatposition">IDvdControl2::ActivateAtPosition</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectatposition">IDvdControl2::SelectAtPosition</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentlocation">IDvdInfo2::GetCurrentLocation</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">IDvdInfo2::GetState</a>. This list may be expanded in the future.

### -field DVD_CacheSizeInMB:6

<div class="alert"><b>Note</b>  Requires Windows Vista or later.</div>
<div> </div>


Specifies how much data the DVD Navigator reads in advance, in MB. For this flag, the <i>bEnable</i> parameter of <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">SetOption</a> is interpreted as a <b>DWORD</b> value, rather than a Boolean.

If the application sets this flag to a large value (&gt; 50 MB), the DVD drive may spin down after the initial pre-fetch, depending on the hardware.

You can also set the cache size by creating the following registry key: <code>HKLM\Software\Microsoft\DVDNavigator\CacheSizeInMB</code>. This registry key is intended for diagnostic purposes only. Applications should use the <b>DVD_CacheSizeInMB</b> flag, not the registry key.

### -field DVD_EnablePortableBookmarks:7

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
<td>DVD bookmarks can be used on another computer. See <a href="/windows/desktop/DirectShow/saving-and-restoring-dvdstate-objects">Saving and Restoring DvdState Objects</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>DVD bookmarks are usable only on the computer where they were created.</td>
</tr>
</table>
 



The default value is <b>FALSE</b>.

### -field DVD_EnableExtendedCopyProtectErrors:8

<div class="alert"><b>Note</b>  Requires Windows Vista or later.
            </div>
<div> </div>


If this flag <b>TRUE</b>, the DVD Navigator supports an extended set of errors related to copy protection failures. These errors are conveyed through the <a href="/windows/desktop/DirectShow/ec-dvd-error">EC_DVD_ERROR</a> event, and include the following:

<ul>
<li>DVD_PB_STOPPED_CopyProtectOutputNotSupported</li>
<li>DVD_PB_STOPPED_CopyProtectOutputFailure</li>
</ul>
(See <a href="/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped">DVD_PB_STOPPED</a>.)

If this flag is <b>FALSE</b>, all copy protection errors are reported using the general <b>DVD_PB_STOPPED_CopyProtectFailure</b> error code.

For backward compatibility, the default value is <b>FALSE</b>.

### -field DVD_NotifyPositionChange:9

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


If this flag is <b>TRUE</b>, the following events are enabled:

<ul>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-program-cell-change">EC_DVD_PROGRAM_CELL_CHANGE</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-program-chain-change">EC_DVD_PROGRAM_CHAIN_CHANGE</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-title-set-change">EC_DVD_TITLE_SET_CHANGE</a>
</li>
</ul>
The default value for this flag is <b>FALSE</b>.

### -field DVD_IncreaseOutputControl:10

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

### -field DVD_EnableStreaming:11

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


Enables or disables <i>streaming mode</i>. In streaming mode, bad blocks on the disc are skipped. The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> receives partially corrected data. This mode generally produces better results when playing scratched or damaged disks, because it results in brief video corruption, rather than long waits that block playback. The DVD drive must support streaming I/O.

The default value is <b>TRUE</b>.

### -field DVD_EnableESOutput:12

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


Enables the <a href="/windows/desktop/DirectShow/data-flow-in-the-dvd-navigator">DVD Navigator</a> to output elementary streams. For more information, see the media types listed in the topic <a href="/windows/desktop/DirectShow/data-flow-in-the-dvd-navigator">DVD Navigator Filter</a>.

The default value is <b>FALSE</b>.

### -field DVD_EnableTitleLength:13

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
[DVD_TitleAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_titleattributes) structure.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">GetTitleAttributes</a> method returns the title mode (karaoke mode or other mode) and not the title length.</td>
</tr>
</table>
 



The default value is <b>FALSE</b>.

### -field DVD_DisableStillThrottle:14

If this flag is <b>TRUE</b>, it disables a call to <code>Sleep(1)</code> that the Navigator otherwise makes when displaying stills.

For backward compatibility, the default value for this flag is <b>FALSE</b>, but the recommended value is <b>TRUE</b>.


<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>

### -field DVD_EnableLoggingEvents:15

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


If this flag is <b>TRUE</b>, the following events are enabled:

<ul>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-beginnavigationcommands">EC_DVD_BeginNavigationCommands</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-gprm-change">EC_DVD_GPRM_Change</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-navigationcommand">EC_DVD_NavigationCommand</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-sprm-change">EC_DVD_SPRM_Change</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-vobu-offset">EC_DVD_VOBU_Offset</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-dvd-vobu-timestamp">EC_DVD_VOBU_Timestamp</a>
</li>
</ul>
The default value for this flag is <b>FALSE</b>.

### -field DVD_MaxReadBurstInKB:16

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


The maximum amount of data that the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> will read ahead in a single burst, in kilobytes. For this flag, the <i>bEnable</i> parameter of <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">SetOption</a> is interpreted as a <b>DWORD</b> value.

The default value is 128 KB.

### -field DVD_ReadBurstPeriodInMS:17

<div class="alert"><b>Note</b>  Requires Windows 7 or later.
            </div>
<div> </div>


How often to perform burst reads into the cache, in milliseconds. For this flag, the <i>bEnable</i> parameter of <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">SetOption</a> is interpreted as a <b>DWORD</b> value.

The default value is 250 milliseconds.

### -field DVD_RestartDisc:18

### -field DVD_EnableCC:19

## -remarks

The following table lists the default values for the Boolean flags.

<table>
<tr>
<th>Flag
            </th>
<th>Default value
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

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a>
