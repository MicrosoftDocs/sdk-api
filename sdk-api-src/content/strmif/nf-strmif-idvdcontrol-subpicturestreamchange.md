---
UID: NF:strmif.IDvdControl.SubpictureStreamChange
title: IDvdControl::SubpictureStreamChange
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects the new subpicture stream and enables or disables it for display.
old-location: dshow\idvdcontrol_subpicturestreamchange.htm
tech.root: DirectShow
ms.assetid: 527031fa-bab9-49f5-89b1-f0c5c5812a76
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDvdControl interface [DirectShow],SubpictureStreamChange method, IDvdControl.SubpictureStreamChange, IDvdControl::SubpictureStreamChange, IDvdControlSubpictureStreamChange, SubpictureStreamChange, SubpictureStreamChange method [DirectShow], SubpictureStreamChange method [DirectShow],IDvdControl interface, dshow.idvdcontrol_subpicturestreamchange, strmif/IDvdControl::SubpictureStreamChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.SubpictureStreamChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IDvdControl.SubpictureStreamChange
: 
---

# IDvdControl::SubpictureStreamChange


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Selects the new subpicture stream and enables or disables it for display.




## -parameters




### -param ulSubPicture

TBD


### -param bDisplay

Value that specifies whether the subpicture is enabled; <b>TRUE</b> makes the subpicture visible and <b>FALSE</b> hides it.


#### - nSubPicture

Value that specifies the source of the subpicture, which must be from 0 through 32, or 63.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0-31</td>
<td>Indicates that the stream is valid.</td>
</tr>
<tr>
<td>32</td>
<td>Enables you to toggle the display without changing the current stream (that is, change <i>bDisplay</i> without altering the current stream).</td>
</tr>
<tr>
<td>63</td>
<td>Indicates that the stream is the dummy stream.</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

