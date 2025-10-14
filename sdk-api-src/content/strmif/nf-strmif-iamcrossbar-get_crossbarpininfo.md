---
UID: NF:strmif.IAMCrossbar.get_CrossbarPinInfo
title: IAMCrossbar::get_CrossbarPinInfo (strmif.h)
description: The get_CrossbarPinInfo method retrieves information about a specified pin.
helpviewer_keywords: ["FALSE","IAMCrossbar interface [DirectShow]","get_CrossbarPinInfo method","IAMCrossbar.get_CrossbarPinInfo","IAMCrossbar::get_CrossbarPinInfo","IAMCrossbarget_CrossbarPinInfo","TRUE","dshow.iamcrossbar_get_crossbarpininfo","get_CrossbarPinInfo","get_CrossbarPinInfo method [DirectShow]","get_CrossbarPinInfo method [DirectShow]","IAMCrossbar interface","strmif/IAMCrossbar::get_CrossbarPinInfo"]
old-location: dshow\iamcrossbar_get_crossbarpininfo.htm
tech.root: dshow
ms.assetid: 29cda12e-a731-4995-8e0c-69dfcda6f158
ms.date: 4/26/2023
ms.keywords: FALSE, IAMCrossbar interface [DirectShow],get_CrossbarPinInfo method, IAMCrossbar.get_CrossbarPinInfo, IAMCrossbar::get_CrossbarPinInfo, IAMCrossbarget_CrossbarPinInfo, TRUE, dshow.iamcrossbar_get_crossbarpininfo, get_CrossbarPinInfo, get_CrossbarPinInfo method [DirectShow], get_CrossbarPinInfo method [DirectShow],IAMCrossbar interface, strmif/IAMCrossbar::get_CrossbarPinInfo
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMCrossbar::get_CrossbarPinInfo
 - strmif/IAMCrossbar::get_CrossbarPinInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMCrossbar.get_CrossbarPinInfo
---

# IAMCrossbar::get_CrossbarPinInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_CrossbarPinInfo</code> method retrieves information about a specified pin.

## -parameters

### -param IsInputPin [in]

Specifies the direction of the pin. Use one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Input pin

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Output pin

</td>
</tr>
</table>

### -param PinIndex [in]

Specifies the index of the pin.

### -param PinIndexRelated [out]

Pointer to a variable that receives the index of the related pin, or –1 if no pin is related to this pin. The <i>related pin</i> is a pin on the same filter, with the same direction; it typically represents the same physical jack or connector. For example, a video tuner and an audio tuner might be related pins. Typically, if two pins are related, you should route them together.

### -param PhysicalType [out]

Pointer to a variable that receives a member of the [PhysicalConnectorType](/windows/desktop/api/strmif/ne-strmif-physicalconnectortype) enumeration, indicating the pin's physical type.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Unknown physical type.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamcrossbar-get_pincounts">IAMCrossbar::get_PinCounts</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar Interface</a>



<a href="/windows/desktop/DirectShow/working-with-crossbars">Working with Crossbars</a>