---
UID: NN:wmp.IWMPSkinManager
title: IWMPSkinManager
author: windows-sdk-content
description: The IWMPSkinManager interface provides a method used to synchronize the current skin with the current desktop theme in Microsoft Windows XP.
old-location: wmp\iwmpskinmanager.htm
old-project: WMP
ms.assetid: c1f27a79-837f-4833-af62-2181406ed725
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSkinManager, IWMPSkinManager interface [Windows Media Player], IWMPSkinManager interface [Windows Media Player],described, IWMPSkinManagerInterface, wmp.iwmpskinmanager, wmp/IWMPSkinManager
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
 - IWMPSkinManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSkinManager interface


## -description



The <b>IWMPSkinManager</b> interface provides a method used to synchronize the current skin with the current desktop theme in Microsoft Windows XP.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSkinManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPSkinManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSkinManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16d0020f-7650-4300-bd34-6f79ecca5175">SetVisualStyle</a>
</td>
<td align="left" width="63%">
Specifies the path to a theme file in Windows XP to which Windows Media Player synchronizes the skin.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPSkinManager</b> interface by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

