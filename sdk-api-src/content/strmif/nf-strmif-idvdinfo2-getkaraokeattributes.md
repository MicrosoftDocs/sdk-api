---
UID: NF:strmif.IDvdInfo2.GetKaraokeAttributes
title: IDvdInfo2::GetKaraokeAttributes
author: windows-sdk-content
description: The GetKaraokeAttributes method retrieves the karaoke attributes of the specified audio stream in the current title or menu.
old-location: dshow\idvdinfo2_getkaraokeattributes.htm
tech.root: DirectShow
ms.assetid: c69ea1e0-8d8a-4cd3-86a4-a2d481160a2e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetKaraokeAttributes, GetKaraokeAttributes method [DirectShow], GetKaraokeAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetKaraokeAttributes method, IDvdInfo2.GetKaraokeAttributes, IDvdInfo2::GetKaraokeAttributes, IDvdInfo2GetKaraokeAttributes, dshow.idvdinfo2_getkaraokeattributes, strmif/IDvdInfo2::GetKaraokeAttributes
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
 - IDvdInfo2.GetKaraokeAttributes
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
- IDvdInfo2.GetKaraokeAttributes
: 
---

# IDvdInfo2::GetKaraokeAttributes


## -description



The <code>GetKaraokeAttributes</code> method retrieves the karaoke attributes of the specified audio stream in the current title or menu.




## -parameters




### -param ulStream [in]

Specifies the index of the audio stream whose attributes you want to query. See Remarks.


### -param pAttributes [out]

Pointer to a <a href="https://msdn.microsoft.com/dffb0b0e-edce-47e7-b9c0-983fdd2c4746">DVD_KaraokeAttributes</a> structure that is filled with the karaoke attributes.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<dt><b>VFW_E_DVD_NOT_IN_KARAOKE_MODE</b></dt>
</dl>
</td>
<td width="60%">
The specified stream is not in karaoke format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not in the title domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The karaoke attributes for the specified stream are not available.

</td>
</tr>
</table>
 




## -remarks



This method does not explicitly return the number of channels in the stream. You can obtain that information through a call to <a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a>. This method is demonstrated in the DVDSample application in <b>CKaraokeDlg::DoModal</b>.

The <i>ulStream</i> parameter may be a value from 0 through 7, or one of the following:

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>DVD_STREAM_DATA_CURRENT (0x800)</td>
<td>To query the currently selected audio stream.</td>
</tr>
<tr>
<td>DVD_DEFAULT_AUDIO_STREAM</td>
<td>To query the default audio stream.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

