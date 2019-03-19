---
UID: NF:strmif.IDvdInfo2.GetAudioAttributes
title: IDvdInfo2::GetAudioAttributes (strmif.h)
author: windows-sdk-content
description: The GetAudioAttributes method retrieves the attributes of the specified audio stream in the current title or menu.
old-location: dshow\idvdinfo2_getaudioattributes.htm
tech.root: DirectShow
ms.assetid: 80291efa-f3eb-47f0-94e0-dcde583ff35c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAudioAttributes, GetAudioAttributes method [DirectShow], GetAudioAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetAudioAttributes method, IDvdInfo2.GetAudioAttributes, IDvdInfo2::GetAudioAttributes, IDvdInfo2GetAudioAttributes, dshow.idvdinfo2_getaudioattributes, strmif/IDvdInfo2::GetAudioAttributes
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
 - IDvdInfo2.GetAudioAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetAudioAttributes


## -description



The <code>GetAudioAttributes</code> method retrieves the attributes of the specified audio stream in the current title or menu.




## -parameters




### -param ulStream [in]

Variable of type ULONG specifying the audio stream whose attributes you wish to query. See Remarks.


### -param pATR [out]

Pointer to a <a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a> structure that is filled with the attributes of the specified audio stream.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The stream's audio attributes are not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



<i>ulStream</i> can be any index number from 0 through 7 or one of the following values:

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>DVD_DEFAULT_AUDIO_STREAM</td>
<td>To query for the attributes of the default audio stream.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_CURRENT</td>
<td>To query the current stream.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VMGM</td>
<td>To query for the VMGM's audio attributes.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VTSM</td>
<td>To query for the VTSM's audio attributes.</td>
</tr>
</table>
 

The use of this method is demonstrated in the DVDSample application in <b>CDvdCore::GetAudioAttributes</b> and <b>CAudioLangDlg::GetAudioLang</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

