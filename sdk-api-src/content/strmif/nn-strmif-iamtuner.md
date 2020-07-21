---
UID: NN:strmif.IAMTuner
title: IAMTuner (strmif.h)
description: The IAMTuner interface controls a TV tuner.
helpviewer_keywords: ["IAMTuner","IAMTuner interface [DirectShow]","IAMTuner interface [DirectShow]","described","IAMTunerInterface","dshow.iamtuner","strmif/IAMTuner"]
old-location: dshow\iamtuner.htm
tech.root: DirectShow
ms.assetid: 997d39c5-a1a5-4d2d-8704-9846f149712c
ms.date: 12/05/2018
ms.keywords: IAMTuner, IAMTuner interface [DirectShow], IAMTuner interface [DirectShow],described, IAMTunerInterface, dshow.iamtuner, strmif/IAMTuner
f1_keywords:
- strmif/IAMTuner
dev_langs:
- c++
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
- IAMTuner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTuner interface


## -description



The <code>IAMTuner</code> interface controls a TV tuner. This interface is the base class for the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner</a> interface, which inherits all of the <code>IAMTuner</code> methods. For more information on controlling a TV tuner using Microsoft DirectShow, see the <b>IAMTVTuner</b> documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTuner</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-channelminmax">ChannelMinMax</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum channel available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-get_channel">get_Channel</a>
</td>
<td align="left" width="63%">
Retrieves the TV channel that the tuner is set to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-get_countrycode">get_CountryCode</a>
</td>
<td align="left" width="63%">
Retrieves the country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-get_mode">get_Mode</a>
</td>
<td align="left" width="63%">
Retrieves the current mode on a multifunction tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-get_tuningspace">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the storage index for regional fine tuning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-getavailablemodes">GetAvailableModes</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's supported modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-logon">Logon</a>
</td>
<td align="left" width="63%">
Logs a user onto the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-logout">Logout</a>
</td>
<td align="left" width="63%">
Logs a user off the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_channel">put_Channel</a>
</td>
<td align="left" width="63%">
Sets the TV channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_countrycode">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code to establish the frequency to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_mode">put_Mode</a>
</td>
<td align="left" width="63%">
Sets a multifunction tuner to the specified mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-put_tuningspace">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Sets a storage index for regional channel-to-frequency mappings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-registernotificationcallback">RegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Allows an object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface to receive event notifications when the tuner changes state. (Not implemented.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-signalpresent">SignalPresent</a>
</td>
<td align="left" width="63%">
Retrieves the strength of the signal on a given channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtuner-unregisternotificationcallback">UnRegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Unregisters an object for event notifications. (Not implemented.)

</td>
</tr>
</table> 

