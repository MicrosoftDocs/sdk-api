---
UID: NN:strmif.IAMTuner
title: IAMTuner
author: windows-sdk-content
description: The IAMTuner interface controls a TV tuner.
old-location: dshow\iamtuner.htm
tech.root: DirectShow
ms.assetid: 997d39c5-a1a5-4d2d-8704-9846f149712c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMTuner, IAMTuner interface [DirectShow], IAMTuner interface [DirectShow],described, IAMTunerInterface, dshow.iamtuner, strmif/IAMTuner
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
 - IAMTuner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner interface


## -description



The <code>IAMTuner</code> interface controls a TV tuner. This interface is the base class for the <a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner</a> interface, which inherits all of the <code>IAMTuner</code> methods. For more information on controlling a TV tuner using Microsoft DirectShow, see the <b>IAMTVTuner</b> documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTuner</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMTuner</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f46bf0ff-cdb3-41b1-829e-4e1b348bd808">ChannelMinMax</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum channel available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68c1b6da-4380-4831-b554-bbb2e3e55ef9">get_Channel</a>
</td>
<td align="left" width="63%">
Retrieves the TV channel that the tuner is set to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b459ad8-c9e0-4b35-aec4-113c8a67d907">get_CountryCode</a>
</td>
<td align="left" width="63%">
Retrieves the country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a5f4cd8-8fde-4777-b9b6-caa7860b005c">get_Mode</a>
</td>
<td align="left" width="63%">
Retrieves the current mode on a multifunction tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/838451c2-2e0b-4a41-a512-f44283573ee6">get_TuningSpace</a>
</td>
<td align="left" width="63%">
Retrieves the storage index for regional fine tuning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74025309-2aab-4e0f-95bc-8e6a1e2a5bb4">GetAvailableModes</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's supported modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4a5a927-254c-44cd-b17d-e1f47b3f62a7">Logon</a>
</td>
<td align="left" width="63%">
Logs a user onto the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/637823ec-0de9-431d-96b7-606abcc9013a">Logout</a>
</td>
<td align="left" width="63%">
Logs a user off the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47ad4288-d855-41cd-b8a2-7b3733a87b41">put_Channel</a>
</td>
<td align="left" width="63%">
Sets the TV channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d733f829-5600-4f75-9bc9-de8dc8dd8031">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code to establish the frequency to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c0691fb-e291-43eb-9828-f58474a4334d">put_Mode</a>
</td>
<td align="left" width="63%">
Sets a multifunction tuner to the specified mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd0c0bc5-2c46-4c5a-8f93-9021f37a6e6a">put_TuningSpace</a>
</td>
<td align="left" width="63%">
Sets a storage index for regional channel-to-frequency mappings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e169039f-bce7-495a-a40f-385fa3d3d2ab">RegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Allows an object that implements the <a href="https://msdn.microsoft.com/8e5fde62-d17c-4d3c-bdb0-0748a9bd285b">IAMTunerNotification</a> interface to receive event notifications when the tuner changes state. (Not implemented.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64a89038-4df1-4e30-8952-6dc039a2e18b">SignalPresent</a>
</td>
<td align="left" width="63%">
Retrieves the strength of the signal on a given channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b46a925b-b4a7-4e2f-aa1b-c98d0f56b33a">UnRegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Unregisters an object for event notifications. (Not implemented.)

</td>
</tr>
</table> 

