---
UID: NN:strmif.IAMTVTuner
title: IAMTVTuner (strmif.h)
author: windows-sdk-content
description: The IAMTVTuner interface controls a TV tuner.
old-location: dshow\iamtvtuner.htm
tech.root: DirectShow
ms.assetid: 1c8300c2-be13-4e4c-aa0c-53ce57bc9152
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTVTuner, IAMTVTuner interface [DirectShow], IAMTVTuner interface [DirectShow],described, IAMTVTunerInterface, dshow.iamtvtuner, strmif/IAMTVTuner
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVTuner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVTuner interface


## -description



The <code>IAMTVTuner</code> interface controls a TV tuner. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/tv-tuner-filter">TV Tuner</a> filter implements this interface. Applications can use this interface to set TV channels and to get or set information about their frequencies, and to determine what analog video standards your TV tuner card supports.

The interface supports tuners for analog broadcast television and AM/FM radio. It supports tuners with multiple input pins, to enable multiple devices and multiple transmission types. The TV Tuner filter supports worldwide tuning coverage. It maps TV channels to specific frequencies through the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_channel">IAMTuner::put_Channel</a> and <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-autotune">IAMTVTuner::AutoTune</a> methods. These methods handle the details of the conversion, so that the hardware driver receives an exact frequency.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTVTuner</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner</a>. <b>IAMTVTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTVTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-autotune">AutoTune</a>
</td>
<td align="left" width="63%">
Scans for a precise signal on the channel's frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_audiofrequency">get_AudioFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the current audio frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_availabletvformats">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves all the analog video TV standards that the tuner supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_connectinput">get_ConnectInput</a>
</td>
<td align="left" width="63%">
Retrieves the hardware tuner input connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_inputtype">get_InputType</a>
</td>
<td align="left" width="63%">
Retrieves the input type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_numinputconnections">get_NumInputConnections</a>
</td>
<td align="left" width="63%">
Retrieves the number of TV sources plugged into the tuner filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_tvformat">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current analog video TV standard in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-get_videofrequency">get_VideoFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the current video frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-put_connectinput">put_ConnectInput</a>
</td>
<td align="left" width="63%">
Sets the hardware tuner input connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-put_inputtype">put_InputType</a>
</td>
<td align="left" width="63%">
Sets the tuner input type (cable or antenna).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtvtuner-storeautotune">StoreAutoTune</a>
</td>
<td align="left" width="63%">
Saves the fine-tuning information for all channels.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/analog-television">Analog Television</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner</a>
 

 

