---
UID: NF:strmif.IDvdControl2.SetSubpictureState
title: IDvdControl2::SetSubpictureState
author: windows-driver-content
description: The SetSubpictureState method turns the subpicture display on or off.
old-location: dshow\idvdcontrol2_setsubpicturestate.htm
old-project: DirectShow
ms.assetid: 2e654bc1-293b-436b-bc33-8a8f269e9aee
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetSubpictureState method, IDvdControl2.SetSubpictureState, IDvdControl2::SetSubpictureState, IDvdControl2SetSubpictureState, SetSubpictureState, SetSubpictureState method [DirectShow], SetSubpictureState method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setsubpicturestate, strmif/IDvdControl2::SetSubpictureState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IDvdControl2.SetSubpictureState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SetSubpictureState


## -description



The <code>SetSubpictureState</code> method turns the subpicture display on or off.




## -parameters




### -param bState [in]

Boolean value that specifies whether the subpicture display is on; <b>TRUE</b> sets subpicture display on for subsequent playback.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is in the First Play domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>
 




## -remarks



Subpicture streams are typically used in menus for button text and sometimes button graphics, and in video playback for subtitles, credits, or other overlaid graphics. Do not confuse subpictures with closed captions; the latter are encoded within the video stream. In general, this method is intended for controlling subpicture display over video while the DVD Navigator filter is playing video in the DVD Title domain.

This method corresponds to the second parameter of the Annex J "Sub-picture_Stream_Change" command.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>
              Annex J Command Name
            </td>
<td>
              Valid Domains
            </td>
</tr>
<tr>
<td>Sub-picture_stream_Change</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/0553a0c4-34d3-4774-9a22-acc01c0a832a">SelectSubpictureStream</a>
 

 

