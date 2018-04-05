---
UID: NN:wmpservices.IWMPMediaPluginRegistrar
title: IWMPMediaPluginRegistrar
author: windows-driver-content
description: The IWMPMediaPluginRegistrar interface manages plug-in registration.
old-location: wmp\iwmpmediapluginregistrar.htm
old-project: WMP
ms.assetid: 4b99d227-39e8-4986-93ed-6df73a3a3e08
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPMediaPluginRegistrar, IWMPMediaPluginRegistrar interface [Windows Media Player], IWMPMediaPluginRegistrar interface [Windows Media Player], described, wmp.iwmpmediapluginregistrar, wmpservices/IWMPMediaPluginRegistrar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmpservices.h
api_name:
-	IWMPMediaPluginRegistrar
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaPluginRegistrar interface


## -description



The <b>IWMPMediaPluginRegistrar</b> interface manages plug-in registration.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMediaPluginRegistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPMediaPluginRegistrar</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/db042911-c46f-431a-ad1c-ceb2c3b4546c">WMPRegisterPlayerPlugin</a>
</td>
<td align="left" width="63%">
Adds information to the registry that identifies a Windows Media Player plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6165962-3ca6-49c8-826c-ce87e55c09fd">WMPUnRegisterPlayerPlugin</a>
</td>
<td align="left" width="63%">
Removes information from the registry about a Windows Media Player plug-in.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4660f928-2e92-468f-9e2b-b411931dfded">DSP Plug-in Interfaces</a>
 

 

