---
UID: NN:wmpplug.IWMPPluginUI
title: IWMPPluginUI
author: windows-driver-content
description: The IWMPPluginUI interface manages the connection to Windows Media Player.
old-location: wmp\iwmppluginui.htm
old-project: WMP
ms.assetid: f292a3e6-87bf-4e68-8737-f7d6351c4ff4
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPluginUI, IWMPPluginUI interface [Windows Media Player], IWMPPluginUI interface [Windows Media Player], described, IWMPPluginUIInterface, wmp.iwmppluginui, wmpplug/IWMPPluginUI
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmpplug.h
api_name:
-	IWMPPluginUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/f7ba2985-42a2-456f-8195-a292c90b440d">Create</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to instantiate the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca78c354-92ae-47d4-82c3-e41eae19f246">Destroy</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to shut down the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29d1438a-164a-460b-9c3e-804417ce362a">DisplayPropertyPage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to request that the plug-in display its property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f01d0700-2399-4e33-8a0c-59bb1f0f2495">GetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve name/value property pairs from the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b6e6878-1d9d-4f45-94a9-316e86da85df">SetCore</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33b36239-3bda-44d3-8f85-7826bd8d3376">SetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to set name/value property pairs for the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0accc3d7-a194-4f89-a90c-ee3ce10d0e27">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Called as part of the Windows Media Player message loop to allow the plug-in to intercept and respond to keyboard events.

</td>
</tr>
</table> 
<div class="alert"><b>Note</b>  Only the <b>SetCore</b> method is supported on Background UI plug-ins in Windows Media Player 10 Mobile.</div><div> </div>

## -see-also




<a href="https://msdn.microsoft.com/5139412c-bafc-4009-82d2-f9c502118c7d">User Interface Plug-ins Programming Reference</a>
 

 

