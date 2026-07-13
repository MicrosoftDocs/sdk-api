---
UID: NF:strmif.IDvdInfo.GetCurrentUOPS
title: IDvdInfo::GetCurrentUOPS (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves which IDvdControl methods are currently valid.
helpviewer_keywords: ["GetCurrentUOPS","GetCurrentUOPS method [DirectShow]","GetCurrentUOPS method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentUOPS method","IDvdInfo.GetCurrentUOPS","IDvdInfo::GetCurrentUOPS","IDvdInfoGetCurrentUOPS","dshow.idvdinfo_getcurrentuops","strmif/IDvdInfo::GetCurrentUOPS"]
old-location: dshow\idvdinfo_getcurrentuops.htm
tech.root: dshow
ms.assetid: a6f48a32-c2bb-4924-9a05-469c7b79fc3e
ms.date: 4/26/2023
ms.keywords: GetCurrentUOPS, GetCurrentUOPS method [DirectShow], GetCurrentUOPS method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentUOPS method, IDvdInfo.GetCurrentUOPS, IDvdInfo::GetCurrentUOPS, IDvdInfoGetCurrentUOPS, dshow.idvdinfo_getcurrentuops, strmif/IDvdInfo::GetCurrentUOPS
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo::GetCurrentUOPS
 - strmif/IDvdInfo::GetCurrentUOPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetCurrentUOPS
---

# IDvdInfo::GetCurrentUOPS


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves which <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl</a> methods are currently valid.

## -parameters

### -param pUOP [out]

Pointer to a <b>DWORD</b> value containing bits for all user operations (UOP). Each bit in the <b>DWORD</b> represents the state (valid or not valid) of a user operation. If the bit corresponding to a user operation is set, then that user operation is prohibited. For more information, see Remarks.

## -returns

Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method is valid in any domain. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

The value of <i>pUOP</i> is a bit field defined as follows.

<table>
<tr>
<th>Bit
            </th>
<th>Flag
            </th>
<th>User function
            </th>
</tr>
<tr>
<td>0</td>
<td>UOP_FLAG_Title_Or_Time_Play</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-titleplay">TitlePlay</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-timeplay">TimePlay</a>
</td>
</tr>
<tr>
<td>1</td>
<td>UOP_FLAG_Chapter_Search_Or_Play</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chaptersearch">ChapterSearch</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chapterplay">ChapterPlay</a>
</td>
</tr>
<tr>
<td>2</td>
<td>UOP_FLAG_Title_Play</td>
<td>TitlePlay</td>
</tr>
<tr>
<td>3</td>
<td>UOP_FLAG_Stop</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-stopforresume">StopForResume</a>
</td>
</tr>
<tr>
<td>4</td>
<td>UOP_FLAG_GoUp</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-goup">GoUp</a>
</td>
</tr>
<tr>
<td>5</td>
<td>UOP_FLAG_Time_Or_Chapter_Search</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-timesearch">TimeSearch</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-chaptersearch">ChapterSearch</a>
</td>
</tr>
<tr>
<td>6</td>
<td>UOP_FLAG_Prev_Or_Top_PG_Search</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-prevpgsearch">PrevPGSearch</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-toppgsearch">TopPGSearch</a>
</td>
</tr>
<tr>
<td>7</td>
<td>UOP_FLAG_Next_PG_Search</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-nextpgsearch">NextPGSearch</a>
</td>
</tr>
<tr>
<td>8</td>
<td>UOP_FLAG_Forward_Scan</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-forwardscan">ForwardScan</a>
</td>
</tr>
<tr>
<td>9</td>
<td>UOP_FLAG_Backward_Scan</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-backwardscan">BackwardScan</a>
</td>
</tr>
<tr>
<td>10</td>
<td>UOP_FLAG_Title_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 2 (DVD_MENU_Title)</td>
</tr>
<tr>
<td>11</td>
<td>UOP_FLAG_Root_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 3 (DVD_MENU_Root)</td>
</tr>
<tr>
<td>12</td>
<td>UOP_FLAG_SubPic_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 4 (DVD_MENU_Subpicture)</td>
</tr>
<tr>
<td>13</td>
<td>UOP_FLAG_Audio_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 5 (DVD_MENU_Audio)</td>
</tr>
<tr>
<td>14</td>
<td>UOP_FLAG_Angle_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 6 (DVD_MENU_Angle)</td>
</tr>
<tr>
<td>15</td>
<td>UOP_FLAG_Chapter_Menu_Call</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> with a parameter value of 7 (DVD_MENU_Chapter)</td>
</tr>
<tr>
<td>16</td>
<td>UOP_FLAG_Resume</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-resume">Resume</a>
</td>
</tr>
<tr>
<td>17</td>
<td>UOP_FLAG_Button_Select_Or_Activate</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-upperbuttonselect">UpperButtonSelect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-lowerbuttonselect">LowerButtonSelect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-leftbuttonselect">LeftButtonSelect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-rightbuttonselect">RightButtonSelect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonactivate">ButtonActivate</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonselectandactivate">ButtonSelectAndActivate</a>
</td>
</tr>
<tr>
<td>18</td>
<td>UOP_FLAG_Still_Off</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-stilloff">StillOff</a>
</td>
</tr>
<tr>
<td>19</td>
<td>UOP_FLAG_Pause_On</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-pauseon">PauseOn</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menulanguageselect">MenuLanguageSelect</a>
</td>
</tr>
<tr>
<td>20</td>
<td>UOP_FLAG_Audio_Stream_Change</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-audiostreamchange">AudioStreamChange</a>
</td>
</tr>
<tr>
<td>21</td>
<td>UOP_FLAG_SubPic_Stream_Change</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-subpicturestreamchange">SubpictureStreamChange</a>
</td>
</tr>
<tr>
<td>22</td>
<td>UOP_FLAG_Angle_Change</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-anglechange">AngleChange</a>, <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-parentallevelselect">ParentalLevelSelect</a>
</td>
</tr>
<tr>
<td>23</td>
<td>UOP_FLAG_Karaoke_Audio_Pres_Mode_Change</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-karaokeaudiopresentationmodechange">KaraokeAudioPresentationModeChange</a>
</td>
</tr>
<tr>
<td>24</td>
<td>UOP_FLAG_Video_Pres_Mode_Change</td>
<td>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-videomodepreferrence">VideoModePreferrence</a>
</td>
</tr>
</table>
 

This method is useful because DVD titles can enable or disable individual user operations at almost any point during playback.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>