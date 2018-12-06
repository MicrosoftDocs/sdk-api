---
UID: NF:mfplay.IMFPMediaPlayer.GetPosition
title: IMFPMediaPlayer::GetPosition
author: windows-sdk-content
description: Gets the current playback position.
old-location: mf\imfpmediaplayer_getposition.htm
tech.root: medfound
ms.assetid: e3401c66-0dc7-46ef-9a38-088d605a3038
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPosition, GetPosition method [Media Foundation], GetPosition method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetPosition method, IMFPMediaPlayer.GetPosition, IMFPMediaPlayer::GetPosition, MFP_POSITIONTYPE_100NS, mf.imfpmediaplayer_getposition, mfplay/IMFPMediaPlayer::GetPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfplay.h
api_name:
 - IMFPMediaPlayer.GetPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetPosition


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current playback position.


## -parameters




### -param guidPositionType [in]

Specifies the unit of time for the playback position. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFP_POSITIONTYPE_100NS"></a><a id="mfp_positiontype_100ns"></a><dl>
<dt><b><b>MFP_POSITIONTYPE_100NS</b></b></dt>
</dl>
</td>
<td width="60%">
100-nanosecond units. 

The value returned in <i>pvPositionValue</i> is a <b>LARGE_INTEGER</b>.

<ul>
<li>Variant type (<b>vt</b>): <b>VT_I8</b></li>
<li>Variant member: <b>hVal</b></li>
</ul>
</td>
</tr>
</table>
 


### -param pvPositionValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the playback position.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
No media item has been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



The playback position is calculated relative to the start time of the media item, which can be specified by calling <a href="https://msdn.microsoft.com/8f0409a6-1911-47ee-ac65-68b87d6b1db5">IMFPMediaItem::SetStartStopPosition</a>. For example, if you set the start time to 20 seconds and the source duration is 60 seconds, the range of values returned by <b>GetPosition</b> is 0–40 seconds.


#### Examples

The following code gets the current position, in 100-nanosecond units, as a <b>LONGLONG</b> value.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT GetPositionHNS(
    IMFPMediaPlayer *pPlayer, 
    LONGLONG *phnsPosition    // Receives the position in hns.
)
{
    HRESULT hr = S_OK;

    PROPVARIANT var;
    PropVariantInit(&amp;var);

    *phnsPosition = 0;

    hr = pPlayer-&gt;GetPosition(MFP_POSITIONTYPE_100NS, &amp;var);

    if (SUCCEEDED(hr))
    {
        *phnsPosition = var.hVal.QuadPart;
    }

    PropVariantClear(&amp;var);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

