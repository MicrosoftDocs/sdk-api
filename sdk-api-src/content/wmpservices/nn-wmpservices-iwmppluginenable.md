---
UID: NN:wmpservices.IWMPPluginEnable
title: IWMPPluginEnable (wmpservices.h)
description: The IWMPPluginEnable interface is implemented by the plug-in. It sets and retrieves a value that represents whether the plug-in has been enabled by Windows Media Player.helpviewer_keywords: ["IWMPPluginEnable","IWMPPluginEnable interface [Windows Media Player]","IWMPPluginEnable interface [Windows Media Player]","described","IWMPPluginEnableInterfaceDSP","wmp.iwmppluginenable","wmpservices/IWMPPluginEnable"]
old-location: wmp\iwmppluginenable.htm
tech.root: WMP
ms.assetid: 997708e2-18fa-436f-9ca1-cdde5c7414fc
ms.date: 12/05/2018
ms.keywords: IWMPPluginEnable, IWMPPluginEnable interface [Windows Media Player], IWMPPluginEnable interface [Windows Media Player],described, IWMPPluginEnableInterfaceDSP, wmp.iwmppluginenable, wmpservices/IWMPPluginEnable
f1_keywords:
- wmpservices/IWMPPluginEnable
dev_langs:
- c++
req.header: wmpservices.h
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
- wmpservices.h
api_name:
- IWMPPluginEnable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPluginEnable interface


## -description



The <b>IWMPPluginEnable</b> interface is implemented by the plug-in. It sets and retrieves a value that represents whether the plug-in has been enabled by Windows Media Player.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPluginEnable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPluginEnable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPluginEnable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmppluginenable-getenable">GetEnable</a>
</td>
<td align="left" width="63%">
Retrieves the current enable state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmppluginenable-setenable">SetEnable</a>
</td>
<td align="left" width="63%">
Sets the current enable state.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/dsp-plug-in-interfaces">DSP Plug-in Interfaces</a>
 

 

