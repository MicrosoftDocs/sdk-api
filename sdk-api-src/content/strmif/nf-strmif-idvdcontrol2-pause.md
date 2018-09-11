---
UID: NF:strmif.IDvdControl2.Pause
title: IDvdControl2::Pause
author: windows-sdk-content
description: Note  This method is deprecated. Applications should call IMediaControl::Pause instead. For more information, see Data Flow in the DVD Navigator. The Pause method pauses or resumes playback at the current location.
old-location: dshow\idvdcontrol2_pause.htm
tech.root: DirectShow
ms.assetid: 32ef572a-56f5-4aa4-b994-08f86a1f17ec
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDvdControl2 interface [DirectShow],Pause method, IDvdControl2.Pause, IDvdControl2::Pause, IDvdControl2Pause, Pause, Pause method [DirectShow], Pause method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_pause, strmif/IDvdControl2::Pause
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
 - IDvdControl2.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::Pause


## -description



<div class="alert"><b>Note</b>  This method is deprecated. Applications should call <a href="https://msdn.microsoft.com/cfb875b7-cc4e-4ae2-8379-964d0e3ceb04">IMediaControl::Pause</a> instead. For more information, see <a href="https://msdn.microsoft.com/14f9cfa3-5ef6-419c-9196-2e4060549c03">Data Flow in the DVD Navigator</a>.</div>
<div> </div>
The <code>Pause</code> method pauses or resumes playback at the current location.




## -parameters




### -param bState [in]

Value of type Boolean that specifies whether to pause playback; <b>TRUE</b> means to pause.


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
UOP control prohibits the DVD Navigator from entering a paused state.

</td>
</tr>
</table>
 




## -remarks



Putting the DVD Navigator into a paused state freezes playback and any internal timers, similar to <a href="https://msdn.microsoft.com/cfb875b7-cc4e-4ae2-8379-964d0e3ceb04">IMediaControl::Pause</a>. If the filter graph is not running, this method does nothing.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Pause_On, Pause_Off</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

