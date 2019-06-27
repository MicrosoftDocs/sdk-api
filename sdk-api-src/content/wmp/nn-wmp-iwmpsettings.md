---
UID: NN:wmp.IWMPSettings
title: IWMPSettings (wmp.h)
author: windows-sdk-content
description: The IWMPSettings interface provides methods that get or set the values of Windows Media Player settings.
old-location: wmp\iwmpsettings.htm
tech.root: WMP
ms.assetid: e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPSettings, IWMPSettings interface [Windows Media Player], IWMPSettings interface [Windows Media Player],described, IWMPSettingsInterface, wmp.iwmpsettings, wmp/IWMPSettings
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPSettings"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings interface


## -description



The <b>IWMPSettings</b> interface provides methods that get or set the values of Windows Media Player settings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSettings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPSettings</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_autostart">get_autoStart</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the current media item begins playing automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_balance">get_balance</a>
</td>
<td align="left" width="63%">
Retrieves the current stereo balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_baseurl">get_baseURL</a>
</td>
<td align="left" width="63%">
Retrieves the base URL used for relative path resolution with URL-type script commands embedded in digital media content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_defaultframe">get_defaultFrame</a>
</td>
<td align="left" width="63%">
Retrieves the name of the frame used to display a URL received in a <b>scriptCommand</b> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_enableerrordialogs">get_enableErrorDialogs</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether error dialog boxes are displayed automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_invokeurls">get_invokeURLs</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether URL events should launch a Web browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_isavailable">get_isAvailable</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether a specified action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_mute">get_mute</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_playcount">get_playCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of times a media item will play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_rate">get_rate</a>
</td>
<td align="left" width="63%">
Retrieves the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_volume">get_volume</a>
</td>
<td align="left" width="63%">
Retrieves the current playback volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-getmode">getMode</a>
</td>
<td align="left" width="63%">
Returns a value indicating whether loop mode or shuffle mode is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_autostart">put_autoStart</a>
</td>
<td align="left" width="63%">
Specifies whether the current media item begins playing automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_balance">put_balance</a>
</td>
<td align="left" width="63%">
Specifies the current stereo balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_baseurl">put_baseURL</a>
</td>
<td align="left" width="63%">
Specifies the base URL used for relative path resolution with URL script commands embedded in digital media files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_defaultframe">put_defaultFrame</a>
</td>
<td align="left" width="63%">
Specifies the name of the frame used to display a URL received in a <b>scriptCommand</b> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_enableerrordialogs">put_enableErrorDialogs</a>
</td>
<td align="left" width="63%">
Specifies whether error dialog boxes are displayed automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_invokeurls">put_invokeURLs</a>
</td>
<td align="left" width="63%">
Specifies whether URL events should launch a Web browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_mute">put_mute</a>
</td>
<td align="left" width="63%">
Specifies whether audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_playcount">put_playCount</a>
</td>
<td align="left" width="63%">
Specifies the number of times a media item will play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_rate">put_rate</a>
</td>
<td align="left" width="63%">
Specifies the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_volume">put_volume</a>
</td>
<td align="left" width="63%">
Specifies the current playback volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-setmode">setMode</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_settings">get_settings</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

