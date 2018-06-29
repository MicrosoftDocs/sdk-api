---
UID: NN:wmp.IWMPSettings
title: IWMPSettings
author: windows-sdk-content
description: The IWMPSettings interface provides methods that get or set the values of Windows Media Player settings.
old-location: wmp\iwmpsettings.htm
old-project: WMP
ms.assetid: e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSettings, IWMPSettings interface [Windows Media Player], IWMPSettings interface [Windows Media Player],described, IWMPSettingsInterface, wmp.iwmpsettings, wmp/IWMPSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
req.include-header: 
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
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings interface


## -description



The <b>IWMPSettings</b> interface provides methods that get or set the values of Windows Media Player settings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37180d0a-8fc4-4fe6-b190-97258803b43b">get_autoStart</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the current media item begins playing automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/457ee1a8-44da-424d-9cc5-0f0421791757">get_balance</a>
</td>
<td align="left" width="63%">
Retrieves the current stereo balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e4a2696-624f-4c6f-8947-2fe0b457332c">get_baseURL</a>
</td>
<td align="left" width="63%">
Retrieves the base URL used for relative path resolution with URL-type script commands embedded in digital media content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/815289bb-4ca5-45da-a27e-7484ba403316">get_defaultFrame</a>
</td>
<td align="left" width="63%">
Retrieves the name of the frame used to display a URL received in a <b>scriptCommand</b> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/557493ea-b685-44e4-b8c3-3f8c5fbe49b8">get_enableErrorDialogs</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether error dialog boxes are displayed automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a29ea1ba-8994-4d0f-8c53-8abba8fe997d">get_invokeURLs</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether URL events should launch a Web browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0773792f-4046-4d58-9673-cbfef0ec5bf5">get_isAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a specified action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0bb1c84-d208-4d29-a797-bb18af039f03">get_mute</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/492eb07a-f757-47ce-8474-1edfeb49e55f">get_playCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times a media item will play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c3f2938-733f-42fc-ae07-66aad715958b">get_rate</a>
</td>
<td align="left" width="63%">
Retrieves the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c217e4-2ec4-4890-810c-dc552a36d578">get_volume</a>
</td>
<td align="left" width="63%">
Retrieves the current playback volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5275cb99-8007-4af2-9137-694de18c5434">getMode</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether loop mode or shuffle mode is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34f80fa4-6e9c-4435-b360-55c2856f89fb">put_autoStart</a>
</td>
<td align="left" width="63%">
Specifies whether the current media item begins playing automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb198bc0-a0cf-4f6b-9a1e-f9a552db7092">put_balance</a>
</td>
<td align="left" width="63%">
Specifies the current stereo balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae070004-e90e-4f1e-b8b8-15deccdc48ad">put_baseURL</a>
</td>
<td align="left" width="63%">
Specifies the base URL used for relative path resolution with URL script commands embedded in digital media files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b035e4e-84c5-46ea-aa8a-2e66810284b2">put_defaultFrame</a>
</td>
<td align="left" width="63%">
Specifies the name of the frame used to display a URL received in a <b>scriptCommand</b> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393">put_enableErrorDialogs</a>
</td>
<td align="left" width="63%">
Specifies whether error dialog boxes are displayed automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c62ba8e-8fca-4cfe-9a52-6b6ac2c7c0de">put_invokeURLs</a>
</td>
<td align="left" width="63%">
Specifies whether URL events should launch a Web browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/644f9a4d-54e4-4e8a-8c02-29feb57c9256">put_mute</a>
</td>
<td align="left" width="63%">
Specifies whether audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9fdd596-8ca3-497e-8d40-6dd5ddbf0a1e">put_playCount</a>
</td>
<td align="left" width="63%">
Specifies the number of times a media item will play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0c395f0-28d1-4c4d-8274-e26c0f4b1ae2">put_rate</a>
</td>
<td align="left" width="63%">
Specifies the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/435dac36-1ccf-41fd-94c2-1242c6af1bbd">put_volume</a>
</td>
<td align="left" width="63%">
Specifies the current playback volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28a404a7-5bb0-41bb-a5b2-cc6138b8176e">setMode</a>
</td>
<td align="left" width="63%">
Sets the loop mode or shuffle mode to active or inactive.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPSettings</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/4bbffaff-99e4-4aae-9b8f-cdb86648fdd9">get_settings</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

