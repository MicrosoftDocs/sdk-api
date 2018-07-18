---
UID: NF:strmif.IDvdInfo.GetTotalTitleTime
title: IDvdInfo::GetTotalTitleTime
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the total playback time for the current title.
old-location: dshow\idvdinfo_gettotaltitletime.htm
old-project: DirectShow
ms.assetid: 90f3a053-edc8-4e42-ae00-31d66d9e3115
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetTotalTitleTime, GetTotalTitleTime method [DirectShow], GetTotalTitleTime method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetTotalTitleTime method, IDvdInfo.GetTotalTitleTime, IDvdInfo::GetTotalTitleTime, IDvdInfoGetTotalTitleTime, dshow.idvdinfo_gettotaltitletime, strmif/IDvdInfo::GetTotalTitleTime
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
 - IDvdInfo.GetTotalTitleTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetTotalTitleTime


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the total playback time for the current title.




## -parameters




### -param pulTotalTime






#### - pTotalTime [out]

Pointer to the total time in <a href="https://msdn.microsoft.com/7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4">DVD_TIMECODE</a> format, which includes hours, minutes, seconds, and frames.


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



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

The method is restricted to simple linear movies by design.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

