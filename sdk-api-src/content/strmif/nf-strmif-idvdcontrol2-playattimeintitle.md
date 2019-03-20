---
UID: NF:strmif.IDvdControl2.PlayAtTimeInTitle
title: IDvdControl2::PlayAtTimeInTitle (strmif.h)
author: windows-sdk-content
description: The PlayAtTimeInTitle method starts playback from the specified time in the specified title.
old-location: dshow\idvdcontrol2_playattimeintitle.htm
tech.root: DirectShow
ms.assetid: 034fa82f-38d2-4031-8d7f-dcf97aa699aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvdControl2 interface [DirectShow],PlayAtTimeInTitle method, IDvdControl2.PlayAtTimeInTitle, IDvdControl2::PlayAtTimeInTitle, IDvdControl2PlayAtTimeInTitle, PlayAtTimeInTitle, PlayAtTimeInTitle method [DirectShow], PlayAtTimeInTitle method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playattimeintitle, strmif/IDvdControl2::PlayAtTimeInTitle
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
 - IDvdControl2.PlayAtTimeInTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::PlayAtTimeInTitle


## -description



The <code>PlayAtTimeInTitle</code> method starts playback from the specified time in the specified title.




## -parameters




### -param ulTitle [in]

Value that specifies the number of the title to play; this value must be from 1 through 99.


### -param pStartTime [in]

Pointer to a <a href="https://msdn.microsoft.com/8f2990f6-a8f5-4b16-ae30-d51ea55496ea">DVD_HMSF_TIMECODE</a> structure that specifies where playback will begin.


### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

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
</table>
 




## -remarks



The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J command name
            </td>
<td>Valid domains
            </td>
</tr>
<tr>
<td>Time_Play</td>
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



<a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>
 

 

