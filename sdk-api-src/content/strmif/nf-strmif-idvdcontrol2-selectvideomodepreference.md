---
UID: NF:strmif.IDvdControl2.SelectVideoModePreference
title: IDvdControl2::SelectVideoModePreference
author: windows-sdk-content
description: The SelectVideoModePreference method sets the specified video mode display (wide screen, letterbox, or pan-scan) for playback.
old-location: dshow\idvdcontrol2_selectvideomodepreference.htm
tech.root: DirectShow
ms.assetid: d970f48e-374f-43de-a59c-6c2e70161f55
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectVideoModePreference method, IDvdControl2.SelectVideoModePreference, IDvdControl2::SelectVideoModePreference, IDvdControl2SelectVideoModePreference, SelectVideoModePreference, SelectVideoModePreference method [DirectShow], SelectVideoModePreference method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectvideomodepreference, strmif/IDvdControl2::SelectVideoModePreference
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
 - IDvdControl2.SelectVideoModePreference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SelectVideoModePreference


## -description



The <code>SelectVideoModePreference</code> method sets the specified video mode display (wide screen, letterbox, or pan-scan) for playback.




## -parameters




### -param ulPreferredDisplayMode [in]

Value that specifies the new display mode for DVD content. Member of the <a href="https://msdn.microsoft.com/afb235ae-ba60-491f-8b88-7fe824f00f77">DVD_PREFERRED_DISPLAY_MODE</a> enumeration.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

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



This method changes the default video window's aspect ratio and can also specify a default aspect ratio conversion mechanism.

For anamorphic 16 x 9 source video, formed by stretching the 720 x 480 source video to a 16 x 9 aspect ratio.

<b>Widescreen</b> The 16 x 9 source video should be placed and stretched into the largest 16 x 9 area of the client output window. The highlights are relative to the inside of the 16 x 9 area. Black bars should be added to either the top/bottom or to the sides to maintain a 16 x 9 area.

<b>Pan Scan</b> The video shown is computed by taking a 4 x 3 subwindow from the stretched 16 x 9 video (the horizontal offset is provided in the MPEG-2 video's window's offset). The 4 x 3 subwindow is placed into the largest 4 x 3 area of the output client window. The highlight's coordinates are relative to the 4 x 3 output window (and have no relationship to the source 16 x 9 video). Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area.

<b>Letterbox</b> A 4 x 3 display area is formed by taking the largest 4 x 3 area of the output client window. Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area. The source 16 x 9 video is placed in the largest 16 x 9 subwindow inside of the 4 x 3 subwindow. Black bars should be added to the top and bottom of the subwindow to maintain a 16 x 9 area. The highlight's coordinates are relative to the 4 x 3 subwindow (and have no relationship to the source 16 x 9 video). It is technically possible for a disk to specify a highlight that lies outside of the 16 x 9 area (but still in the 4 x 3 window).

For 4 x 3 video, the video is placed in the largest 4 x 3 output area of the output client window. Black bars should be added to either the top/bottom or to the sides to maintain a 4 x 3 area.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Video_Presentation_Mode_Change</td>
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
 

 

