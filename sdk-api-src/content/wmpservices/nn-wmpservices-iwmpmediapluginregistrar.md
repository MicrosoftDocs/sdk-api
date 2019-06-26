---
UID: NN:wmpservices.IWMPMediaPluginRegistrar
title: IWMPMediaPluginRegistrar (wmpservices.h)
author: windows-sdk-content
description: The IWMPMediaPluginRegistrar interface manages plug-in registration.
old-location: wmp\iwmpmediapluginregistrar.htm
tech.root: WMP
ms.assetid: 4b99d227-39e8-4986-93ed-6df73a3a3e08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPMediaPluginRegistrar, IWMPMediaPluginRegistrar interface [Windows Media Player], IWMPMediaPluginRegistrar interface [Windows Media Player],described, wmp.iwmpmediapluginregistrar, wmpservices/IWMPMediaPluginRegistrar
ms.topic: interface
f1_keywords: 
 - "wmpservices/IWMPMediaPluginRegistrar"
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
 - IWMPMediaPluginRegistrar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMediaPluginRegistrar interface


## -description



The <b>IWMPMediaPluginRegistrar</b> interface manages plug-in registration.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMediaPluginRegistrar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPMediaPluginRegistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMediaPluginRegistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin">WMPRegisterPlayerPlugin</a>
</td>
<td align="left" width="63%">
Adds information to the registry that identifies a Windows Media Player plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin">WMPUnRegisterPlayerPlugin</a>
</td>
<td align="left" width="63%">
Removes information from the registry about a Windows Media Player plug-in.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/dsp-plug-in-interfaces">DSP Plug-in Interfaces</a>
 

 

