---
UID: NN:wmpplug.IWMPPluginUI
title: IWMPPluginUI
author: windows-sdk-content
description: The IWMPPluginUI interface manages the connection to Windows Media Player.
old-location: wmp\iwmppluginui.htm
tech.root: WMP
ms.assetid: f292a3e6-87bf-4e68-8737-f7d6351c4ff4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPluginUI, IWMPPluginUI interface [Windows Media Player], IWMPPluginUI interface [Windows Media Player],described, IWMPPluginUIInterface, wmp.iwmppluginui, wmpplug/IWMPPluginUI
ms.topic: interface
req.header: wmpplug.h
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
 - wmpplug.h
api_name:
 - IWMPPluginUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPluginUI interface


## -description



The <b>IWMPPluginUI</b> interface manages the connection to Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPluginUI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPPluginUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPluginUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563592(v=VS.85).aspx">Create</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to instantiate the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563593(v=VS.85).aspx">Destroy</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to shut down the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563594(v=VS.85).aspx">DisplayPropertyPage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to request that the plug-in display its property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563595(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve name/value property pairs from the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563596(v=VS.85).aspx">SetCore</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563597(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to set name/value property pairs for the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563598(v=VS.85).aspx">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Called as part of the Windows Media Player message loop to allow the plug-in to intercept and respond to keyboard events.

</td>
</tr>
</table> 
<div class="alert"><b>Note</b>  Only the <b>SetCore</b> method is supported on Background UI plug-ins in Windows Media Player 10 Mobile.</div><div> </div>

## -see-also




<a href="https://msdn.microsoft.com/5139412c-bafc-4009-82d2-f9c502118c7d">User Interface Plug-ins Programming Reference</a>
 

 

