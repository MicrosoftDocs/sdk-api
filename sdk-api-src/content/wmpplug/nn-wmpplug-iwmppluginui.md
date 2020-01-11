---
UID: NN:wmpplug.IWMPPluginUI
title: IWMPPluginUI (wmpplug.h)
description: The IWMPPluginUI interface manages the connection to Windows Media Player.
old-location: wmp\iwmppluginui.htm
tech.root: WMP
ms.assetid: f292a3e6-87bf-4e68-8737-f7d6351c4ff4
ms.date: 12/05/2018
ms.keywords: IWMPPluginUI, IWMPPluginUI interface [Windows Media Player], IWMPPluginUI interface [Windows Media Player],described, IWMPPluginUIInterface, wmp.iwmppluginui, wmpplug/IWMPPluginUI
f1_keywords:
- wmpplug/IWMPPluginUI
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPluginUI interface


## -description



The <b>IWMPPluginUI</b> interface manages the connection to Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPluginUI</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPluginUI</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-create">Create</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to instantiate the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to shut down the plug-in user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage">DisplayPropertyPage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to request that the plug-in display its property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve name/value property pairs from the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setcore">SetCore</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to provide plug-in access to the core Windows Media Player APIs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to set name/value property pairs for the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Called as part of the Windows Media Player message loop to allow the plug-in to intercept and respond to keyboard events.

</td>
</tr>
</table> 
<div class="alert"><b>Note</b>  Only the <b>SetCore</b> method is supported on Background UI plug-ins in Windows Media Player 10 Mobile.</div><div> </div>

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/user-interface-plug-ins-programming-reference">User Interface Plug-ins Programming Reference</a>
 

 

