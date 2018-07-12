---
UID: NF:strmif.IDvdInfo.GetCurrentUOPS
title: IDvdInfo::GetCurrentUOPS
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves which IDvdControl methods are currently valid.
old-location: dshow\idvdinfo_getcurrentuops.htm
old-project: DirectShow
ms.assetid: a6f48a32-c2bb-4924-9a05-469c7b79fc3e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetCurrentUOPS, GetCurrentUOPS method [DirectShow], GetCurrentUOPS method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentUOPS method, IDvdInfo.GetCurrentUOPS, IDvdInfo::GetCurrentUOPS, IDvdInfoGetCurrentUOPS, dshow.idvdinfo_getcurrentuops, strmif/IDvdInfo::GetCurrentUOPS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetCurrentUOPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetCurrentUOPS


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves which <a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl</a> methods are currently valid.




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
Requested action is not supported on this domain (<a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>).

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



This method is valid in any domain. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

The value of <i>pUOP</i> is a bit field defined as follows.

<table>
<tr>
<th>
              Bit
            </th>
<th>
              Flag
            </th>
<th>
              User function
            </th>
</tr>
<tr>
<td>0</td>
<td>UOP_FLAG_Title_Or_Time_Play</td>
<td>
<a href="https://msdn.microsoft.com/5ca710f0-8f08-43d6-8cc1-a25068d5e0ef">TitlePlay</a>, <a href="https://msdn.microsoft.com/56b4b086-e315-486c-8dbd-97960f5b76d1">TimePlay</a>
</td>
</tr>
<tr>
<td>1</td>
<td>UOP_FLAG_Chapter_Search_Or_Play</td>
<td>
<a href="https://msdn.microsoft.com/1389df65-e269-4c2b-b276-a29da33fe515">ChapterSearch</a>, <a href="https://msdn.microsoft.com/c51524d0-5935-4e14-bcaf-4739fd0f21bb">ChapterPlay</a>
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
<a href="https://msdn.microsoft.com/61c5b863-038b-4c4a-a7a4-d1fd1801f843">StopForResume</a>
</td>
</tr>
<tr>
<td>4</td>
<td>UOP_FLAG_GoUp</td>
<td>
<a href="https://msdn.microsoft.com/2a553a5f-f221-4161-95f1-cb1629abb87a">GoUp</a>
</td>
</tr>
<tr>
<td>5</td>
<td>UOP_FLAG_Time_Or_Chapter_Search</td>
<td>
<a href="https://msdn.microsoft.com/c2e6848e-569e-44f0-b676-e22e4df07d8d">TimeSearch</a>, <a href="https://msdn.microsoft.com/1389df65-e269-4c2b-b276-a29da33fe515">ChapterSearch</a>
</td>
</tr>
<tr>
<td>6</td>
<td>UOP_FLAG_Prev_Or_Top_PG_Search</td>
<td>
<a href="https://msdn.microsoft.com/8e2d0531-23be-471b-8094-d21771209c79">PrevPGSearch</a>, <a href="https://msdn.microsoft.com/35a621de-5110-4999-8475-ae84a4dc9ee1">TopPGSearch</a>
</td>
</tr>
<tr>
<td>7</td>
<td>UOP_FLAG_Next_PG_Search</td>
<td>
<a href="https://msdn.microsoft.com/a509f63f-a3e9-4b49-bbf0-f59051db119a">NextPGSearch</a>
</td>
</tr>
<tr>
<td>8</td>
<td>UOP_FLAG_Forward_Scan</td>
<td>
<a href="https://msdn.microsoft.com/dedeec1c-8565-491e-ab2c-4cdc17d988a9">ForwardScan</a>
</td>
</tr>
<tr>
<td>9</td>
<td>UOP_FLAG_Backward_Scan</td>
<td>
<a href="https://msdn.microsoft.com/9d2b1635-9b02-465a-a725-8b7985b651fb">BackwardScan</a>
</td>
</tr>
<tr>
<td>10</td>
<td>UOP_FLAG_Title_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 2 (DVD_MENU_Title)</td>
</tr>
<tr>
<td>11</td>
<td>UOP_FLAG_Root_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 3 (DVD_MENU_Root)</td>
</tr>
<tr>
<td>12</td>
<td>UOP_FLAG_SubPic_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 4 (DVD_MENU_Subpicture)</td>
</tr>
<tr>
<td>13</td>
<td>UOP_FLAG_Audio_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 5 (DVD_MENU_Audio)</td>
</tr>
<tr>
<td>14</td>
<td>UOP_FLAG_Angle_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 6 (DVD_MENU_Angle)</td>
</tr>
<tr>
<td>15</td>
<td>UOP_FLAG_Chapter_Menu_Call</td>
<td>
<a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> with a parameter value of 7 (DVD_MENU_Chapter)</td>
</tr>
<tr>
<td>16</td>
<td>UOP_FLAG_Resume</td>
<td>
<a href="https://msdn.microsoft.com/336908bb-369e-449d-a94a-dd22fa72f20a">Resume</a>
</td>
</tr>
<tr>
<td>17</td>
<td>UOP_FLAG_Button_Select_Or_Activate</td>
<td>
<a href="https://msdn.microsoft.com/bd0e4086-087b-460f-a6af-fa073644f1bb">UpperButtonSelect</a>, <a href="https://msdn.microsoft.com/eba476a5-c949-4ce1-b296-314e36afc912">LowerButtonSelect</a>, <a href="https://msdn.microsoft.com/62c35cb1-f1e0-4852-9a59-555cf979615f">LeftButtonSelect</a>, <a href="https://msdn.microsoft.com/67ca86cd-37a7-48ce-80d9-585d345e83fc">RightButtonSelect</a>, <a href="https://msdn.microsoft.com/6a5ee6ed-2baa-45d6-a874-5df4e5c56841">ButtonActivate</a>, <a href="https://msdn.microsoft.com/15ed6a4e-d798-49c9-bff3-c77207658d31">ButtonSelectAndActivate</a>
</td>
</tr>
<tr>
<td>18</td>
<td>UOP_FLAG_Still_Off</td>
<td>
<a href="https://msdn.microsoft.com/0f466728-027e-40d6-b8f8-ed0aad02dd1e">StillOff</a>
</td>
</tr>
<tr>
<td>19</td>
<td>UOP_FLAG_Pause_On</td>
<td>
<a href="https://msdn.microsoft.com/d67a7a16-41f9-4718-a6ad-d48ba77fb1d4">PauseOn</a>, <a href="https://msdn.microsoft.com/6b5c660c-3d3f-4f78-8eca-3a42982eb0ae">MenuLanguageSelect</a>
</td>
</tr>
<tr>
<td>20</td>
<td>UOP_FLAG_Audio_Stream_Change</td>
<td>
<a href="https://msdn.microsoft.com/08fca00b-e187-40db-99c0-8b978dd0f10e">AudioStreamChange</a>
</td>
</tr>
<tr>
<td>21</td>
<td>UOP_FLAG_SubPic_Stream_Change</td>
<td>
<a href="https://msdn.microsoft.com/527031fa-bab9-49f5-89b1-f0c5c5812a76">SubpictureStreamChange</a>
</td>
</tr>
<tr>
<td>22</td>
<td>UOP_FLAG_Angle_Change</td>
<td>
<a href="https://msdn.microsoft.com/4a91f05d-1ded-4ecb-8850-5ee7faad134d">AngleChange</a>, <a href="https://msdn.microsoft.com/ca572d89-b188-442d-884f-0cffa71c2892">ParentalLevelSelect</a>
</td>
</tr>
<tr>
<td>23</td>
<td>UOP_FLAG_Karaoke_Audio_Pres_Mode_Change</td>
<td>
<a href="https://msdn.microsoft.com/a724af67-6aac-4307-97bc-a79e73621ce1">KaraokeAudioPresentationModeChange</a>
</td>
</tr>
<tr>
<td>24</td>
<td>UOP_FLAG_Video_Pres_Mode_Change</td>
<td>
<a href="https://msdn.microsoft.com/9e68b09c-534c-46d2-bda0-72f3d1d86b66">VideoModePreferrence</a>
</td>
</tr>
</table>
 

This method is useful because DVD titles can enable or disable individual user operations at almost any point during playback.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

